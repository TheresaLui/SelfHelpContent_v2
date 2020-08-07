<properties
	pageTitle="How to Perform Key Vault actions"
	description="How to Perform Key Vault actions"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="ShaneBala-keyvault"
	ms.author="sudbalas"
	displayOrder="5"
	selfHelpType="generic"
	supportTopicIds="32738119, 32738115, 32738120, 32738117"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-howother2"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to Perform Key Vault actions

## **Recommended Documents**
* [Integrate Key Vault with Kubernetes](https://docs.microsoft.com/azure/key-vault/general/key-vault-integrate-kubernetes)
* [Integrate Key Vault with Databricks](https://docs.microsoft.com/azure/key-vault/general/integrate-databricks-blob-storage)

## **Recommended Steps**

* [Key Vault Get Started](https://docs.microsoft.com/azure/key-vault/key-vault-overview)
* [About Key Vault](https://docs.microsoft.com/azure/key-vault/basic-concepts)
* [Key Vault Best Practices](https://docs.microsoft.com/azure/key-vault/key-vault-best-practices)
* [Developer's Guide](https://docs.microsoft.com/azure/key-vault/key-vault-developers-guide)

### **Troubleshooting**

* If key is in deleted state, you can recover or purge secret. If your vault has purge protection, you can recover and create new version of key or wait for purge protection period to be over : [Soft-deleted Secret Operations](https://docs.microsoft.com/azure/key-vault/general/soft-delete-cli#secrets) 
* Key Vault returns HTTP status code 429 (Too many requests): [Key Vault Throttling options](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-throttling)
* If you have problem with access to key vault, make sure that you have access policy created: [Key Vault Access Policies](https://docs.microsoft.com/azure/key-vault/general/group-permissions-for-apps)
* If you have problem with authenticate to key vault in code, use [Authentication SDK](https://azure.github.io/azure-sdk/posts/2020-02-25/defaultazurecredentials.html) 
