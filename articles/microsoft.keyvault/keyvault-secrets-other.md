<properties
	pageTitle="How to Perform Key Vault actions"
	description="How to Perform Key Vault actions"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="jlichwa"
	ms.author="jalichwa"
	displayOrder="5"
	selfHelpType="generic"
	supportTopicIds="32738116"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-secrets-other"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to Perform Key Vault actions
## **Recommended Steps**

* [Key Vault Get Started](https://docs.microsoft.com/azure/key-vault/key-vault-overview)
* [About Secrets](https://docs.microsoft.com/azure/key-vault/secrets/about-secrets)
* [Key Vault Best Practices](https://docs.microsoft.com/azure/key-vault/key-vault-best-practices)
* [Developer's Guide](https://docs.microsoft.com/azure/key-vault/key-vault-developers-guide)

### **Troubleshooting**

**Troubleshooting**

* If secret is in deleted state, you can recover or purge secret. If your vault has purge protection, you can recover and create new version of secret or wait for purge protection period to be over : [Soft-deleted Secret Operations](https://docs.microsoft.com/azure/key-vault/general/soft-delete-cli#secrets) 
* Key Vault returns HTTP status code 429 (Too many requests): [Key Vault Throttling options](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-throttling)
* If you have problem with access to key vault, make sure that you have access policy created: [Key Vault Access Policies](https://docs.microsoft.com/azure/key-vault/general/group-permissions-for-apps)
* If you have problem with authenticate to key vault in code, use [Authentication SDK](https://azure.github.io/azure-sdk/posts/2020-02-25/defaultazurecredentials.html) 


## **Recommended Documents**

* [Adding secret using CLI](https://docs.microsoft.com/azure/key-vault/secrets/quick-create-cli#add-a-secret-to-key-vault)
* [Use Secrets with Azure DevOps](https://docs.microsoft.com/azure/devops/pipelines/library/variable-groups?view=azure-devops&tabs=yaml#link-secrets-from-an-azure-key-vault)
* [Use Secrets with Azure App Service](https://docs.microsoft.com/azure/app-service/app-service-key-vault-references)
