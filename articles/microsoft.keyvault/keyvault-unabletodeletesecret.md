<properties
	pageTitle="Unable to delete secret"
	description="Unable to delete secret"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="jalichwa"
	displayOrder="19"
	selfHelpType="generic"
	supportTopicIds="32742808"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-unabletodeletesecret"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Unable to Delete Secret

## **Recommended Steps**

* Check if you have delete access permission to key vault: [Key Vault Access Policies](https://docs.microsoft.com/azure/key-vault/general/group-permissions-for-apps)
* If secret is in deleted state, you can recover or purge secret. If your vault has purge protection, you can recover and create new version of secret or wait for purge protection period to be over. Purge protection period cannot be changed : [Soft-deleted Secret Operations](https://docs.microsoft.com/azure/key-vault/general/soft-delete-cli#secrets) 

**Troubleshooting**

* Key Vault returns HTTP status code 429 (Too many requests): [Key Vault Throttling options](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-throttling)

* If you have problem with authenticate to key vault in code, use [Authentication SDK](https://azure.github.io/azure-sdk/posts/2020-02-25/defaultazurecredentials.html) 

## **Recommended Documents**

* Use preferred language from supported list [Developer's Guide](https://docs.microsoft.com/azure/key-vault/general/developers-guide)
