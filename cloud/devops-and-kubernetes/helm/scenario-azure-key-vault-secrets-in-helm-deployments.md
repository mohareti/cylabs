# Scenario: Azure Key Vault Secrets in Helm Deployments

##

Azure Key Vault is a cloud service for securely storing and accessing secrets. When deploying applications in Kubernetes using Helm, integrating Azure Key Vault for managing sensitive data like API client IDs and secrets is a best practice. Below is a brief explanation and steps to set this up.

### Brief Explanation

* **Azure Key Vault**: A tool for securely storing and accessing secrets, keys, and certificates.
* **Helm Values**: Used to pass configurations to a Helm chart. Sensitive data like API keys can be stored in Azure Key Vault and referenced in Helm deployments.

### Configuration Steps

#### 1. Login to Azure

First, ensure you have the Azure CLI installed and then log in:

```bash
az login
```

This command will open a web browser asking for your Azure credentials.

#### 2. Create a Resource Group

Create a resource group if you don’t have one:

```bash
az group create --name <ResourceGroupName> --location <Location>
```

#### 3. Create Azure Key Vault

Create a Key Vault in your resource group:

```bash
az keyvault create --name <YourKeyVaultName> --resource-group <ResourceGroupName> --location <Location>
```

#### 4. Add Secrets to Key Vault

Store your API client ID and secret in the Key Vault:

```bash
az keyvault secret set --vault-name <YourKeyVaultName> --name "<SecretName1>" --value "<ClientID>"
az keyvault secret set --vault-name <YourKeyVaultName> --name "<SecretName2>" --value "<ClientSecret>"
```

#### 5. Assign Access Policy

Assign an access policy to allow your application to read secrets from the Key Vault:

```bash
az keyvault set-policy --name <YourKeyVaultName> --object-id <ObjectID> --secret-permissions get list
```

#### 6. Using Secrets in Helm Deployments

When deploying your application with Helm, you’ll need to ensure that your application can access these secrets. This can be done in several ways, depending on your cluster configuration and security practices.

* **Directly in Helm Values** (not recommended for sensitive data): You can reference secrets directly in your `values.yaml` file, but this method is not secure for sensitive data like API keys.
* **Environment Variables in Kubernetes**: More securely, you can set up your application to read these secrets as environment variables. The secrets are not directly written in the Helm chart but are injected into your pods from the Key Vault using tools like [Azure Key Vault to Kubernetes](https://github.com/SparebankenVest/azure-key-vault-to-kubernetes) (akv2k8s).
* **CSI Secret Store**: Another approach is to use the [Secrets Store CSI driver](https://github.com/kubernetes-sigs/secrets-store-csi-driver) for Azure, which enables mounting Key Vault secrets as volumes in Kubernetes.
* **Template Reference**: In your Helm chart templates, you can reference these environment variables or mounted volumes to configure your application.

### Conclusion

Integrating Azure Key Vault with Helm deployments in Kubernetes adds an essential layer of security for managing sensitive data. By storing API client IDs and secrets in Azure Key Vault and securely referencing them in Helm charts, you can maintain the confidentiality and integrity of your application’s sensitive configuration data.
