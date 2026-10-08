---
description: "Kubernetes, also known as K8s, is an open-source platform designed to automate deploying, scaling, and operating application containers."
---

# Kubernetes 101

Kubernetes, also known as K8s, is an open-source platform designed to automate deploying, scaling, and operating application containers. It was originally developed by Google and is now maintained by the Cloud Native Computing Foundation. Kubernetes makes it easier to manage containerized applications across different environments, whether it's on-premises, in the public cloud, or a hybrid mix.

#### Core Components of Kubernetes

1. **Control Plane (Master Node)**:
   * **API Server**: The front-end for the Kubernetes control plane; it exposes the Kubernetes API.
   * **etcd**: A consistent and highly-available key-value store used to store all cluster data.
   * **Scheduler**: Watches for newly created pods with no assigned node and selects a node for them to run on.
   * **Controller Manager**: Runs controller processes, handling node failure, replicating pods, and more.
   * **Cloud Controller Manager**: Lets you link your cluster into the cloud provider's API.
2. **Worker Nodes**:
   * **Kubelet**: An agent that runs on each node in the cluster, ensuring that containers are running in a Pod.
   * **Kube-Proxy**: Maintains network rules on nodes, allowing network communication to your Pods.
   * **Container Runtime**: The software responsible for running containers (e.g., Docker).
3. **Pods**:
   * The smallest deployable units in Kubernetes, which can host one or multiple containers.

#### Installation

The complexity of installing Kubernetes can vary based on the environment and specific needs. For beginners, Minikube is a popular way to create a small Kubernetes cluster locally on your machine.

* **Minikube**:
  * Install Minikube from the [official website](https://minikube.sigs.k8s.io/docs/start/).
  * It simplifies running a single-node Kubernetes cluster in a virtual machine on your laptop.
* **Kubectl**:
  * You also need to install `kubectl`, a command-line tool for interacting with the Kubernetes cluster.
  * Download and install instructions are available on the [Kubernetes official documentation](https://kubernetes.io/docs/tasks/tools/).

#### Common and Useful Kubernetes Commands

* **General Management**:
  * `kubectl get nodes`: Lists all nodes in the cluster.
  * `kubectl get pods`: Lists all pods in the current namespace.
  * `kubectl get deployments`: Lists all deployments.
* **Pod Management**:
  * `kubectl run [name] --image=[image]`: Starts a new pod with a specified name and image.
  * `kubectl delete pod [name]`: Deletes a specific pod.
  * `kubectl describe pod [name]`: Shows detailed information about a specific pod.
* **Deployment and Service**:
  * `kubectl create -f [config_file.yaml]`: Creates a resource specified in a YAML configuration file.
  * `kubectl delete -f [config_file.yaml]`: Deletes the resource specified in a YAML configuration file.
  * `kubectl expose deployment [name] --type="NodePort" --port [port]`: Exposes your application to an external IP address.
* **Debugging and Diagnostics**:
  * `kubectl logs [pod_name]`: Fetches logs from a specific pod.
  * `kubectl exec -it [pod_name] -- /bin/bash`: Executes an interactive bash shell on a specified pod.
* **Configuration**:
  * `kubectl apply -f [config_file.yaml]`: Applies a configuration to a resource from a file.
* **Cluster Info**:
  * `kubectl cluster-info`: Displays information about the cluster.
  * `kubectl config view`: Shows the Kubernetes configuration.

#### Conclusion

Kubernetes is a powerful tool for container orchestration, offering both high flexibility and control over how applications run and interact. It's widely used in the industry due to its robust feature set and community support. For anyone working with containerized applications, especially in a microservices architecture, understanding and utilizing Kubernetes is increasingly becoming essential.

Kubernetes and Docker are both crucial components in the world of containerized application development and deployment, but they serve different purposes and function in different layers of the container ecosystem. Understanding the differences between them is key to effectively using containers in your software development and operations.

#### Docker

1. **Core Functionality**:
   * Docker is a containerization platform that enables developers to package applications and their dependencies into a standardized unit for software development. It encapsulates the application and its environment.
2. **Primary Focus**:
   * The main focus of Docker is to create, deploy, and run applications by using containers. Docker provides the runtime environment for containers, handling the packaging and distribution of the application.
3. **Scope**:
   * Docker operates at a single-container level. It is mainly used to containerize applications, ensuring consistency across multiple development and release cycles.
4. **Components**:
   * Docker includes Docker Engine, Docker Images, Docker Containers, Docker Hub, and Docker Compose for managing individual containers.
5. **Use Case**:
   * Ideal for the development phase and for single-container setups. It simplifies the process of creating and managing containers.
6. **Community and Ecosystem**:
   * Docker has a vast ecosystem with a large repository of container images available on Docker Hub. It is widely adopted for containerization tasks.

#### Kubernetes

1. **Core Functionality**:
   * Kubernetes, on the other hand, is an orchestration tool for managing multiple containers at scale. It is designed to coordinate clusters of nodes at scale in production in an efficient manner.
2. **Primary Focus**:
   * Kubernetes focuses on the deployment, scaling, and operations of application containers across clusters of hosts. It deals with high-level concepts involving groups of containers, networking, and orchestration.
3. **Scope**:
   * Kubernetes is not about running a single container; it's about scaling containers across multiple hosts, managing them as a single unit, and automating their deployment.
4. **Components**:
   * Kubernetes includes a range of components like Pods, Deployments, Services, Nodes, and more, offering a robust framework for managing containerized applications.
5. **Use Case**:
   * Ideal for production environments. Kubernetes excels in managing complex applications with multiple containers, handling auto-scaling, load-balancing, and self-healing.
6. **Community and Ecosystem**:
   * Kubernetes has a strong community support and ecosystem, being part of the Cloud Native Computing Foundation (CNCF). It is widely supported across various cloud platforms.

#### Key Differences

* **Level of Abstraction**: Docker is at the container level, focusing on packaging and running containers, while Kubernetes is at the cluster level, focusing on orchestrating and managing containers across multiple machines.
* **Complexity and Scalability**: Docker simplifies container creation and management, suitable for simpler workflows. Kubernetes, being more complex, is designed for larger, distributed systems.
* **Interoperability**: Kubernetes can manage containers that run on Docker, as well as on other container runtime environments.

In summary, Docker is about creating and managing individual containers, whereas Kubernetes is about managing clusters of containers. They often work together, with Docker providing a great environment for managing a container's lifecycle, and Kubernetes providing a platform for managing and orchestrating Docker containers.
