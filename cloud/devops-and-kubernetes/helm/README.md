# Helm

## Comprehensive Guide to Package Management in Kubernetes with Helm

Package management is a critical aspect of software development and deployment, including in Kubernetes environments. Helm is a widely used package manager for Kubernetes, streamlining the installation and management of applications.

### What is Package Management in Kubernetes?

In Kubernetes, package management involves the handling of Kubernetes applications, including their deployment, configuration, updating, and lifecycle management. Kubernetes applications often comprise multiple resources like Deployments, Services, ConfigMaps, and Persistent Volume Claims. Managing these resources as a single unit and maintaining consistency across environments can be challenging, which is where package management tools like Helm come into play.

### What is Helm?

Helm is an open-source package manager for Kubernetes, often described as the `apt/yum/homebrew` for Kubernetes. It simplifies the process of defining, installing, and upgrading even the most complex Kubernetes applications.

#### Helm Use Cases

* **Simplifying Application Deployment**: Packages complex Kubernetes applications into easy-to-deploy units.
* **Managing Application Dependencies**: Manages dependencies for Kubernetes applications.
* **Versioning and Rollbacks**: Allows versioning of Kubernetes applications and supports easy rollbacks to previous versions.
* **Customizing Deployments**: Offers customizable installations through Helm charts.

#### Helm Components and Resources

* **Helm Chart**: A collection of files that describe a related set of Kubernetes resources. A single chart might be used to deploy something simple, like a memcached pod, or something complex, like a full web app stack.
* **Helm Repository**: A place where charts can be collected and shared. It's like a package archive.
* **Helm Release**: An instance of a chart running in a Kubernetes cluster. One chart can often be installed many times into the same cluster, with each installation called a release.

#### Installation Steps

1. **Download Helm**: Visit the [Helm releases page](https://github.com/helm/helm/releases) and download the appropriate version for your operating system.
2. **Unpack the Helm binary** and add it to your PATH.
3. **Initialize Helm and Install Tiller** (only for Helm v2):
   * Run `helm init` to install Tiller, the server-side component of Helm. (Note: Tiller is not used in Helm v3.)
4. **Verify Installation**: Run `helm version` to check if Helm is installed correctly.

#### Where to Get Helm Charts

* **Artifact Hub**: A CNCF-hosted repository for finding shared Helm charts.
* **Official Helm Charts GitHub**: Helm charts maintained by the Helm community.

#### Example to Deploy Helm Chart

* **Installing an existing Chart**:

  ```bash
  helm repo add bitnami https://charts.bitnami.com/bitnami
  helm install my-release bitnami/nginx
  ```
* This command installs the Nginx server from the Bitnami repository.

#### Helm 2 vs Helm 3

* **Tiller**: Helm 2 uses Tiller on the cluster to manage charts, while Helm 3 is tiller-less, improving security and operation simplicity.
* **Release Names**: Helm 3 release names are scoped to the namespace level, not the cluster level.
* **Improved Upgrade Strategy**: Helm 3 supports three-way strategic merge patches.
* **Secrets as the Default Storage Driver**: Helm 3 uses Secrets as the default storage driver for release information.

#### Widely Used Helm Commands

* `helm install`: Install a chart.
* `helm upgrade`: Upgrade a release.
* `helm rollback`: Rollback to a previous version of a release.
* `helm list`: List releases.
* `helm uninstall`: Uninstall a release.
* `helm repo add`: Add a chart repository.
* `helm search repo`: Search for charts in a repository.

### Conclusion

Helm streamlines the deployment and management of applications in Kubernetes, addressing many of the complexities associated with managing multiple Kubernetes resources. Understanding Helm’s architecture, components, and basic commands is crucial for anyone managing applications in Kubernetes. As Helm continues to evolve, especially with the transition from v2 to v3, it remains a vital tool in the Kubernetes ecosystem.

### References

1. <https://learn.microsoft.com/en-us/azure/aks/quickstart-helm?tabs=azure-cli>
2. <https://learn.microsoft.com/en-us/azure/aks/kubernetes-helm>

## In this section

* ✅ [Scenario: Azure Key Vault Secrets in Helm Deployments](scenario-azure-key-vault-secrets-in-helm-deployments.md)
