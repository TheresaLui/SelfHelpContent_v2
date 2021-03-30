<properties
  pagetitle="Managing an Existing Key Vault&#xD;"
  service="microsoft.keyvault"
  resource="vaults"
  ms.author="jalichwa,sebansal"
  selfhelptype="Generic"
  supporttopicids="32375296"
  resourcetags="optional"
  productpesids="15657"
  cloudenvironments="blackforest,fairfax,public,mooncake,usnat,ussec"
  articleid="ef2146e8-0e56-4e59-b7fa-629446d88d7f"
  ownershipid="AzureKeyVault_KeyVault" />
# Managing an Existing Key Vault

## **Recommended Steps**

* [Create and manage Key Vault with CLI](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
* [Secure your Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-secure-your-key-vault)<br>

### Troubleshoot Key Vault issues

* How can I back up Key Vault or Key Vault objects?<br>
  You can back up individual Key Vault objects, for example, Backup Key, Backup Secret, Backup Certificate, by [using Azure CLI](https://docs.microsoft.com/rest/api/keyvault/backupkey), [Using Powershell](https://docs.microsoft.com/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey?view=azurermps-6.13.0). The backup command backs up old versions of each secret. If you have a secret with a large number of previous versions (more than 10), the request size might exceed the allowed maximum and the operation might fail.

* To move a key vault, see these resources:
    - [Moving an Azure Key Vault across resource groups](https://docs.microsoft.com/azure/key-vault/general/move-resourcegroup)
    - [Moving an Azure Key Vault to another subscription](https://docs.microsoft.com/azure/key-vault/general/move-subscription)
    - [Moving an Azure key vault across regions](https://docs.microsoft.com/azure/key-vault/general/move-region)
    - [Change a Key Vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/general/move-subscription#additional-steps-when-subscription-is-in-a-new-tenant)

* I have several (over 16) applications that need to access a key vault. How can I add multiple access policies?<br>

Key Vault supports up to **1024** access policy entries, with each entry granting a distinct set of permissions to a particular security principal. See [grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Using Soft-Delete with Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)<br>
* [Key Vault key rotation and auditing](https://docs.microsoft.com/azure/key-vault/key-vault-key-rotation-log-monitoring)<br>
* [Key Vault Developer's Guide](https://docs.microsoft.com/azure/key-vault/key-vault-developers-guide)
