<properties
	pageTitle="Using Key Vault with Soft Delete"
	description="Using Key Vault with Soft Delete"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="ShaneBala-keyvault"
	ms.author="sudbalas"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32596891"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-howother"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Using Key Vault with Soft Delete

## **Recommended Steps**

* **BREAKING CHANGE** To enhance the level of protection that Microsoft offers for your secrets stored in key vault, soft delete will no longer be an opt-out feature. Soft-delete will be required to be enabled on all Azure key vaults. **Starting in December 2020 you will no longer be able to create a new key vault with soft-delete disabled.** Please see the following document that details this change and turn on soft delete protection on all of your key vaults: [Soft Delete Always On](https://docs.microsoft.com/azure/key-vault/general/soft-delete-change).

* [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/general/key-vault-recovery?tabs=azure-portal)

### **Troubleshooting**

* If you deleted a key vault it will exist in the soft-deleted state if you had soft-delete enabled on the key vault and the retention period has not elapsed. **If you did not have soft delete enabled, or the soft delete retention period has elapsed, your key vault has been permanently deleted and it is impossible for you or Microsoft to recover your key vault.** Use the following references to list and recover a deleted key vault:

	* [List deleted Key Vaults](https://docs.microsoft.com/cli/azure/keyvault?view=azure-cli-latest#az-keyvault-list-deleted)
	* [Recover a deleted Key Vault](https://docs.microsoft.com/cli/azure/keyvault?view=azure-cli-latest#az-keyvault-recover)
	
* If you deleted a secret, key, or certificate it will exist in the soft-deleted state if you had soft-delete enabled on the key vault and the retention period has not elapsed. **If soft delete was not enabled on the key vault or the retention period has elapsed, your secret has been permanently deleted and it is impossible for you or Microsoft to recover your secret.** Use the following references to recover:

	* [Recover a deleted certificate](https://docs.microsoft.com/cli/azure/keyvault/certificate?view=azure-cli-latest#az-keyvault-certificate-recover)
	* [Recover a deleted key](https://docs.microsoft.com/cli/azure/keyvault/key?view=azure-cli-latest#az-keyvault-key-recover)
	* [Recover a deleted secret](https://docs.microsoft.com/cli/azure/keyvault/secret?view=azure-cli-latest#az-keyvault-secret-recover)

* Please note that turning on soft-delete and purge protection are one-time operations on each key vault. **It is not possible for you or for Microsoft to disable soft-delete or purge protection once the features have been enabled on a key vault.** You must wait for the mandatory retention period to elapse before you will be able to permanently delete your key vault or secrets.

## **Recommended Documents**

* [Soft Delete Overview](https://docs.microsoft.com/azure/key-vault/general/key-vault-recovery?tabs=azure-portal)<br>
* [Using Soft-Delete with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)<br>
* [Understanding Backup and Restore Behavior in Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-security-worlds)<br>
