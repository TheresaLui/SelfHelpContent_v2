<properties
	pageTitle="Unable to Retrieve Secrets"
	description="Unable to Retrieve Secrets"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="jalichwa"
	displayOrder="19"
	selfHelpType="generic"
	supportTopicIds="32742809"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-unabletoretrievesecret"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Unable to Retrieve Secrets

## **Recommended Steps**

* If you have problem with access to key vault, make sure that you have access policy created: [Key Vault Access Policies](https://docs.microsoft.com/azure/key-vault/general/group-permissions-for-apps)

**Troubleshooting**

* If secret is in deleted state, you can recover or purge secret. If your vault has purge protection, you can recover and create new version of secret or wait for purge protection period to be over : [Soft-deleted Secret Operations](https://docs.microsoft.com/azure/key-vault/general/soft-delete-cli#secrets) 
* Key Vault returns HTTP status code 429 (Too many requests): [Key Vault Throttling options](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-throttling)

* If you have problem with authenticate to key vault in code, use [Authentication SDK](https://azure.github.io/azure-sdk/posts/2020-02-25/defaultazurecredentials.html) 

## **Recommended Documents**

* Use preferred language from supported list [Developer's Guide](https://docs.microsoft.com/azure/key-vault/general/developers-guide)
