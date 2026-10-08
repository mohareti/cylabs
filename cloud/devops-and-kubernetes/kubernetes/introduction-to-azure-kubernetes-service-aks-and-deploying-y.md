# Introduction to Azure Kubernetes Service (AKS) and Deploying Your First Cluster

##

Azure Kubernetes Service (AKS) is a managed container orchestration service provided by Microsoft Azure, which simplifies the deployment, management, and operations of Kubernetes. It eliminates the complexity of managing Kubernetes by offloading much of that responsibility to Azure. This guide will walk you through creating your first AKS cluster and deploying a sample application.

### What is AKS?

AKS provides a hosted Kubernetes environment, making it easier to deploy and manage containerized applications without container orchestration expertise. It automates tasks such as hardware provisioning, software updates, scaling, and more.

### Creating Your First AKS Cluster

#### Prerequisites

* An Azure account. If you don’t have one, you can create a [free account](https://azure.microsoft.com/en-us/free/).
* Azure CLI installed. You can download it from [here](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli).

#### Steps to Create an AKS Cluster

1. **Login to Azure**:
   * Open a terminal or command prompt and log into your Azure account using the Azure CLI:

     ```bash
     az login
     ```
2. **Create a Resource Group**:
   * AKS clusters are created within an Azure resource group. Create one using the Azure CLI:

     ```bash
     az group create --name myResourceGroup --location eastus
     ```
3. **Create AKS Cluster**:
   * Create your AKS cluster using the following command:

     ```bash
     az aks create --resource-group myResourceGroup --name myAKSCluster --node-count 1 --enable-addons monitoring --generate-ssh-keys
     ```
   * This command creates an AKS cluster named `myAKSCluster` with one node.
4. **Configure `kubectl` to Use Your AKS Cluster**:
   * Get the credentials for your cluster:

     ```bash
     az aks get-credentials --resource-group myResourceGroup --name myAKSCluster
     ```
   * This step updates your `kubectl` config file with the new cluster’s details.

### Deploying a Sample Application

1. **Create a Deployment**:
   * You can deploy a sample application to your AKS cluster using `kubectl`. For example, you can deploy a basic NGINX server:

     ```bash
     kubectl create deployment nginx --image=nginx
     ```
2. **Expose the NGINX Deployment**:
   * Expose the NGINX pod to the internet using the `kubectl expose` command:

     ```bash
     kubectl expose deployment nginx --port=80 --type=LoadBalancer
     ```
   * This command creates an Azure Load Balancer with a public IP address to access your NGINX server.
3. **Access Your Application**:
   * Get the external IP address for your NGINX service:

     ```bash
     kubectl get service nginx
     ```
   * Once the external IP address is available, you can access your NGINX server using the IP address in a web browser.

### Conclusion

AKS simplifies Kubernetes management, allowing you to focus on building your applications rather than managing the underlying infrastructure. By following these steps, you can easily create an AKS cluster and deploy a sample application, paving the way for more complex deployments and management tasks. For more detailed information and advanced configurations, refer to the [AKS documentation](https://docs.microsoft.com/en-us/azure/aks/).
