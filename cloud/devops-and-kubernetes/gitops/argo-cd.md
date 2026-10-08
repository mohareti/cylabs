# Argo CD

### Argo CD Installation Steps and Commands

Deploying a Helm chart from Azure Repos or a public GitHub repository with Argo CD involves several steps, including setting up Argo CD in your Kubernetes cluster, connecting it to your repositories, and then deploying your applications using Helm charts. Here's a step-by-step guide to walk you through the process:

#### 1. Install Argo CD in Your Kubernetes Cluster

1. **Create the Argo CD Namespace**:

   ```bash
   kubectl create namespace argocd
   ```
2. **Install Argo CD**:

   ```bash
   kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
   ```
3. **Access Argo CD**:
   * By default, the Argo CD API server is not exposed externally. To access it, use port-forwarding:

     ```bash
     kubectl port-forward svc/argocd-server -n argocd 8080:443
     ```
   * The Argo CD UI can then be accessed at `https://localhost:8080`.
4. **Login to Argo CD**:
   * The initial password for the `admin` account is auto-generated. To retrieve it, use:

     ```bash
     kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
     ```
   * Login using the CLI:

     ```bash
     argocd login localhost:8080
     ```

#### 2. Connect Argo CD to Azure Repos and GitHub

1. **Add Azure Repos as a Repository**:

   * Use the Argo CD CLI or UI to add your Azure Repos repository. You’ll need the repository URL and authentication credentials (if it's a private repo).

   ```bash
   argocd repo add <Azure_Repo_URL> --username <username> --password <password>
   ```
2. **Add GitHub Repository**:

   * For a public GitHub repository, authentication is not required:

   ```bash
   argocd repo add <GitHub_Repo_URL>
   ```

#### 3. Deploy Applications Using Helm Charts

1. **Create an Application in Argo CD**:

   * This can be done via the CLI or the UI. You’ll need to specify the details of your Helm chart. For example:

   ```bash
   argocd app create <app-name> \
   --repo <Repo_URL> \
   --path <path_to_chart> \
   --dest-server https://kubernetes.default.svc \
   --dest-namespace <namespace>
   ```
2. **Sync the Application**:

   * Once the application is created, synchronize it to deploy the Helm chart:

   ```bash
   argocd app sync <app-name>
   ```
3. **Verify Deployment**:

   * Check the status of your application in Argo CD:

   ```bash
   argocd app get <app-name>
   ```

   * Or view it in the Argo CD UI.

#### 4. Manage and Update Deployments

* **Update Your Chart**: Make changes to your Helm chart in Azure Repos or GitHub. Argo CD will detect these changes and can automatically sync them based on your configuration.
* **Manual Sync**: For manual sync, use the `argocd app sync` command again or use the UI.

#### Conclusion

Deploying Helm charts from Azure Repos and GitHub using Argo CD provides a powerful way to manage Kubernetes applications declaratively. Argo CD's ability to integrate with different version control systems and automate application deployment and lifecycle management makes it a valuable tool in the GitOps toolkit. Remember to manage your secrets and sensitive data securely when working with public repositories and CI/CD pipelines.

Creating an Argo CD application to deploy a guestbook example using Terraform involves writing a Terraform script that defines the necessary Kubernetes resources. Below is an example Terraform script that creates an Argo CD application for deploying a guestbook application.

Before you start, ensure you have:

* Terraform installed and configured.
* Access to a Kubernetes cluster with Argo CD installed.
* `kubectl` configured to interact with your Kubernetes cluster.

#### Terraform Script to Create an Argo CD Application

First, create a Terraform configuration file (e.g., `argo_app.tf`):

```hcl
provider "kubernetes" {
  # Configuration options
}

resource "kubernetes_manifest" "argo_cd_app" {
  manifest = {
    apiVersion = "argoproj.io/v1alpha1"
    kind       = "Application"
    metadata = {
      name      = "guestbook"
      namespace = "argocd"
    }
    spec = {
      project = "default"

      source = {
        repoURL        = "https://github.com/argoproj/argocd-example-apps.git"
        targetRevision = "HEAD"
        path           = "guestbook"
      }

      destination = {
        server    = "https://kubernetes.default.svc"
        namespace = "guestbook"
      }

      syncPolicy = {
        automated = {
          prune    = false
          selfHeal = false
        }
      }
    }
  }
}
```

This script defines a Kubernetes manifest for an Argo CD application. The application is configured to deploy the guestbook app from the [argoproj/argocd-example-apps](https://github.com/argoproj/argocd-example-apps) repository.

#### Steps to Deploy the Application

1. **Initialize Terraform**: Navigate to the directory containing your Terraform script and run:

   ```bash
   terraform init
   ```

   This command initializes Terraform in the directory.
2. **Apply the Terraform Configuration**: Deploy the Argo CD application with:

   ```bash
   terraform apply
   ```

   Confirm the action when prompted. Terraform will create the Argo CD application in your Kubernetes cluster.
3. **Check the Application**: Verify that the application is created in Argo CD:

   ```bash
   kubectl get applications -n argocd
   ```

   You should see the `guestbook` application listed.

#### Additional Notes

* **Namespace**: The script assumes that Argo CD is installed in the `argocd` namespace. Adjust accordingly if your setup differs.
* **Sync Policy**: The `syncPolicy` is set to not automatically sync. You can change this by setting `prune` and `selfHeal` to `true` if desired.
* **Provider Configuration**: Replace the provider block with your cluster's specific configuration details.

Using Terraform to manage Argo CD applications allows you to treat your deployment configurations as code, enabling versioning, repeatability, and integration into CI/CD pipelines.

References

1. <https://thomasdecaux.medium.com/deploy-a-kubernetes-gitops-ready-aks-terraform-argocd-193e61d19d05>
2. <https://foxutech.medium.com/setup-argocd-on-azure-kubernetes-services-9c3fa543f4b6>
3. <https://techcommunity.microsoft.com/t5/apps-on-azure-blog/getting-started-with-gitops-argo-and-azure-kubernetes-service/ba-p/3288595>
