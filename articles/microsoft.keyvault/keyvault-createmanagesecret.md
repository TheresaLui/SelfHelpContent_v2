<properties
	pageTitle="How to Create and Manage Secrets"
	description="How to Create and Manage Secrets"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="jalichwa"
	displayOrder="19"
	selfHelpType="generic"
	supportTopicIds="32739894"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-createmanagesecrets"
	ownershipId="AzureKeyVault_KeyVault"
/>

# How to Create and Manage Secrets

## **Recommended Steps**

* Use appropriate method from recommended documents to create secret. If secret name exists, new version of secret will be created.

**Troubleshooting**

* If secret is in deleted state, you can recover or purge secret. If your vault has purge protection, you can recover and create new version of secret or wait for purge protection period to be over : [Soft-deleted Secret Operations](https://docs.microsoft.com/azure/key-vault/general/soft-delete-cli#secrets) 
* Key Vault returns HTTP status code 429 (Too many requests): [Key Vault Throttling options](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-throttling)
* If you have problem with access to key vault, make sure that you have access policy created: [Key Vault Access Policies](https://docs.microsoft.com/azure/key-vault/general/group-permissions-for-apps)
* If you have problem with authenticate to key vault in code, use [Authentication SDK](https://azure.github.io/azure-sdk/posts/2020-02-25/defaultazurecredentials.html) 

## **Recommended Documents**

* [Adding secret using CLI](https://docs.microsoft.com/azure/key-vault/secrets/quick-create-cli#add-a-secret-to-key-vault)
* [Add Secrets to Key Vault with Azure Portal](https://docs.microsoft.com/azure/key-vault/secrets/quick-create-portal#add-a-secret-to-key-vault)
* [Add Secrets to Key Vault with .NET](https://docs.microsoft.com/azure/key-vault/secrets/quick-create-net#save-a-secret)
* Use preferred language from supported list [Developer's Guide](https://docs.microsoft.com/azure/key-vault/general/developers-guide)
