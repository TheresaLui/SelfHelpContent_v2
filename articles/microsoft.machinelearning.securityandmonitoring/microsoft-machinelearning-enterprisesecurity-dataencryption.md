<properties
	pageTitle="Data Encryption"
	description="Data Encryption"
	infoBubbleText="Data Encryption"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
	supportTopicIds="32740869"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.enterprisesecurity.dataencryption"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Data Encryption

Azure Machine Learning encrypts all your data at rest and in transit using Microsoft-managed keys. Additional steps you can take to further secure your data include:

1. Creating a high business impact (HBI) enabled workspace.
2. Using customer-managed keys for encryption via Azure Key Vault.

Follow the reccommended steps to learn more about how to enable each feature.

## **Recommended Steps**

### **High Business Impact (HBI)**

An HBI-enabled workspace controls the amount of data Microsoft collects for diagnostic purposes and enables additional encryption in Microsoft managed environments. In addition it enables the following:

- Encrypts the local scratch disk in your AML compute clusters.
- Cleans up your local scratch disk between runs
- Securely passes credentials for your storage account, container registry and SSH account from the execution layer to your compute clusters using your key vault
- Enables IP filtering to ensure the underlying batch pools cannot be called by any external services other than Azure Machine Learning service

To create an HBI-enabled workspace, set the `hbi_workspace` parameter to True in the <a href="https://docs.microsoft.com/python/api/azureml-core/azureml.core.workspace(class)?view=azure-ml-py#create-name--auth-none--subscription-id-none--resource-group-none--location-none--create-resource-group-true--sku--basic---friendly-name-none--storage-account-none--key-vault-none--app-insights-none--container-registry-none--cmk-keyvault-none--resource-cmk-uri-none--hbi-workspace-false--default-cpu-compute-target-none--default-gpu-compute-target-none--private-endpoint-config-none--private-endpoint-auto-approval-true--exist-ok-false--show-output-true-">Workspace.create()</a> method.

### **Customer-managed Keys**

To manage your own keys for encrypting data at rest and in transit, you will need to add them to an [Azure Key Vault](https://azure.microsoft.com/services/key-vault/). Then you will need to attach the key vault to the corresponding resources where you'd like to use them. See the following [article](https://docs.microsoft.com/azure/machine-learning/concept-enterprise-security#data-encryption) for detailed instructions.

## **Recommended Documents**

Here is a list of additional resources which may be helpful: 

* [Enterprise security overview](https://docs.microsoft.com/azure/machine-learning/concept-enterprise-security)
* [Azure data encryption at rest](https://docs.microsoft.com/azure/security/fundamentals/encryption-atrest)
* [Azure Storage encryption with customer-managed keys](https://docs.microsoft.com/azure/storage/common/storage-encryption-keys-portal)
* [CosmoDB encryption with customer-managed keys](https://docs.microsoft.com/azure/cosmos-db/how-to-setup-cmk)
* [Azure Kubernetes service encryption with customer-managed keys](https://docs.microsoft.com/azure/aks/azure-disk-customer-managed-keys)
