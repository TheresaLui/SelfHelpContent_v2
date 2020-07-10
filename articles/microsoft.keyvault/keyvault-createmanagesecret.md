<properties
	pageTitle="How to Create and Manage Secrets"
	description="How to Create and Manage Secrets"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="sudbalas"
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

* For a tutorial on how to create and retrieve secrets, see the tutorial link in the **Recommended Documents** section below. 

* If you have a secret stored in your key vault and attempt to create a new secret with the same name, the create operation will create a new version of the original secret. Please make sure the name of your secret is unique if you do not want this behavior. 

* If you recently deleted a secret, it may exist in the soft deleted state. Attempting to create a secret with the same name will result in a conflict. Please see the **Troubleshooting** section below to resolve this error.

* Some secret names are hidden and reserved. For example, when you create a certificate object named 'cert1' in key vault, the private key of the certificate is stored as a hidden secret with the same name. Attempting to create a secret with the name 'cert1' will result in a conflict. 

* If you are getting a 429 response code, your key vault operations are being throttled. Please see the **Troubleshooting** section for guidance. 

**Troubleshooting**

* To verify and resolve a conflict with a soft deleted secret, you must recover or purge the deleted secret. 
	* Verify secret is in Soft Deleted State [List Deleted Secret](https://docs.microsoft.com/cli/azure/keyvault/secret?view=azure-cli-latest#az-keyvault-secret-list-deleted)
	* Recover deleted secret [Recover Deleted Secret](https://docs.microsoft.com/cli/azure/keyvault/secret?view=azure-cli-latest#az-keyvault-secret-recover)
	* Purge deleted secret [Purge Deleted Secret](https://docs.microsoft.com/cli/azure/keyvault/secret?view=azure-cli-latest#az-keyvault-secret-purge) This operation requires the 'purge secret' access policy permission. Purge protection must be disabled on the key vault. 

* Key Vault returns HTTP status code 429 (Too many requests): [Key Vault Throttling options](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-throttling)

* If you have problem with access to key vault, make sure that you have access policy created: [Key Vault Access Policies](https://docs.microsoft.com/azure/key-vault/general/group-permissions-for-apps)

* If you have problem with authenticate to key vault in code, use [Authentication SDK](https://azure.github.io/azure-sdk/posts/2020-02-25/defaultazurecredentials.html) 

## **Recommended Documents**

* [Set and retrieve a secret tutorial PowerShell](https://docs.microsoft.com/azure/key-vault/secrets/quick-create-powershell)
* [Adding secret using CLI](https://docs.microsoft.com/azure/key-vault/secrets/quick-create-cli#add-a-secret-to-key-vault)
* [Add Secrets to Key Vault with Azure Portal](https://docs.microsoft.com/azure/key-vault/secrets/quick-create-portal#add-a-secret-to-key-vault)
* [Add Secrets to Key Vault with .NET](https://docs.microsoft.com/azure/key-vault/secrets/quick-create-net#save-a-secret)
* Use preferred language from supported list [Developer's Guide](https://docs.microsoft.com/azure/key-vault/general/developers-guide)
