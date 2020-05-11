<properties
	pageTitle="Lost or Deleted Keys and Secrets in Key Vault"
	description="Using Soft-Delete and Backup and Restore Behavior with Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="ShaneBala-keyvault"
	ms.author="sudbalas"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32375295"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="ac9233e4-9d2f-4aa4-87cd-68ef92f61952-res"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Lost or Deleted Keys and Secrets in Key Vault
## **Recommended Steps**

* [Using Soft-Delete and Backup and Restore Behavior with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)

### **Troubleshooting**

* If you deleted a key vault it will exist in the soft-deleted state if you had soft-delete enabled on the key vault and the retention period has not elapsed. **If you did not have soft delete enabled, or the soft delete retention period has elapsed, your key vault has been permanently deleted and it is impossible for you or Microsoft to recover your key vault.** Use the following references to list and recover a deleted key vault.

	* [List deleted Key Vaults](https://docs.microsoft.com/cli/azure/keyvault?view=azure-cli-latest#az-keyvault-list-deleted)
	* [Recover a deleted Key Vault](https://docs.microsoft.com/cli/azure/keyvault?view=azure-cli-latest#az-keyvault-recover)
	
* If you deleted a secret, key, or certificate it will exist in the soft-deleted state if you had soft-delete enabled on the key vault and the retention period has not elapsed. **If soft delete was not enabled on the key vault or the retention period has elapsed, your secret has been permanently deleted and it is impossible for you or Microsoft to recover your secret.** Use the following references to recover. 
	* [Recover a deleted certificate](https://docs.microsoft.com/cli/azure/keyvault/certificate?view=azure-cli-latest#az-keyvault-certificate-recover)
	* [Recover a deleted key](https://docs.microsoft.com/cli/azure/keyvault/key?view=azure-cli-latest#az-keyvault-key-recover)
	* [Recover a deleted secret](https://docs.microsoft.com/cli/azure/keyvault/secret?view=azure-cli-latest#az-keyvault-secret-recover)

* Please note that turning on soft-delete and purge protection are one-time operations on each key vault. **It is not possible for you or for Microsoft to disable soft-delete or purge protection once the features have been enabled on a key vault.** You must wait for the mandatory retention period to elapse before you will be able to permanently delete your key vault or secrets.

## **Recommended Documents**

* [Using Soft-Delete with Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)<br>
* [Using Soft-Delete with Key Vault with CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-cli)<br>
* [Using Soft-Delete with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)<br>
* [Understanding Backup and Restore Behavior in Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-security-worlds)<br>
