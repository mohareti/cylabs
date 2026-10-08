# Wazuh on Azure AKS

Deployment of Wazuh infrastructure on Azure AKS, architecting using  GitOps + IaaC

## Prerequisites

* Cloud Service Provider **Azure**
* Containerization **Kubernetes**
* Managed Kubernetes Cluster Service **Azure Kubernetes Service**
* Infrastructure as a Code **Terraform**
* Git Ops **Argo CD**
* Kubernetes Package management **Helm Chart**

Roadmap

1. **Azure Configuration**
   * **Azure account:** Set up an Azure account with required subscriptions and permissions.
   * **AKS cluster:** Create an AKS cluster with appropriate scale and security settings. Consider Managed Identity for easier integration.
   * **Persistent storage:** Decide on a persistent storage solution (Azure Managed Disks, Azure Files) for Wazuh data.

2. **Create a Git repository to store your Terraform code.**

   * Define Terraform configurations to,
     * Provision Azure AKS cluster
       * Configure AKS with appropriate node pool configurations, such as node sizes, availability zones, and node count.
       * Enable Kubernetes RBAC for secure access control.
       * integrate AKS with Azure Monitor for monitoring and logging.
     * Networking components
     * Key vault
   * Configure Terraform backend to store state securely (e.g., Azure Storage Account).
   * Implement Terraform modules for reusability and maintainability.

3. **Helm Chart for Wazuh:**
   *  Helm charts for deploying Wazuh components (Wazuh manager, Wazuh agents, Elasticsearch, Kibana, etc.).
   * Customize Helm chart values to match your specific requirements, such as configuration settings, storage options, and resource limits.

4. **Integration with Azure DevOps:**
   * Set up Azure DevOps pipelines for CI/CD.
   * Configure a pipeline for building and pushing Docker images for Wazuh components to a container registry (e.g., Azure Container Registry).
   * Create pipeline tasks for deploying infrastructure using Terraform scripts.
   * Integrate Helm chart deployment tasks into the pipeline for deploying Wazuh components to the AKS cluster.

5. **GitOps Workflow with Argo CD:**
   * Install Argo CD on the AKS cluster using Helm charts.
   * Configure Argo CD to watch the Git repositories containing Helm chart manifests and Kubernetes manifests for Wazuh.
   * Set up Argo CD Applications to deploy and manage Wazuh components using Helm charts.
   * Define GitOps policies for automatic synchronization and reconciliation of the desired state with the actual state in the AKS cluster.

6. **Continuous Deployment and Delivery:**
   * Trigger Azure DevOps pipelines automatically on code commits or schedule them for periodic runs.
   * Utilize Argo CD's continuous deployment capabilities to automatically deploy and update Wazuh components based on changes in the Git repositories.
   * Implement testing and validation stages in the pipeline to ensure the stability and correctness of deployments.
   * Monitor pipeline execution and application health using Azure DevOps monitoring tools and Azure Monitor.

7. **Security and Compliance Considerations:**
   * Implement security best practices for AKS, such as network policies, Pod Security Policies, and Azure Security Center recommendations.
   * Enable encryption at rest and in transit for data stored in Elasticsearch.
   * Configure Wazuh rules and policies for threat detection and compliance monitoring.
   * Integrate Azure Key Vault for secure management of secrets and sensitive configuration data.

## References

{% embed url="<https://kubernetes.io/docs/home/>" %}

{% embed url="<https://helm.sh/>" %}

{% embed url="<https://argo-cd.readthedocs.io/en/stable/>" %}

{% embed url="<https://azure.microsoft.com/en-us/products/kubernetes-service>" %}

{% embed url="<https://documentation.wazuh.com/current/deployment-options/deploying-with-kubernetes/index.html>" %}

{% embed url="<https://github.com/wazuh/wazuh-kubernetes>" %}

{% embed url="<https://developer.hashicorp.com/terraform/tutorials/azure-get-started>" %}
