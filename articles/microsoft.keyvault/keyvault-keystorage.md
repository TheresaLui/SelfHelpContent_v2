<properties
	pageTitle="Key Storage with Key Vault"
	description="Key Storage with Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="11"
	selfHelpType="resource"
	supportTopicIds="32375280"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# 4 Ways to Store Keys with Key Vault
## **Recommended steps**

* Please make sure you have installed [PowerShell](https://www.powershellgallery.com/packages/AzureRM/4.1.0). Below are 4 methods for storing keys in a key vault.<br>
* Import key into a key vault.<br>
    ```
        $key = Add-AzureKeyVaultKey -VaultName 'ContosoKeyVault' -Name 'ContosoFirstKey' -KeyFilePath 'c:\softkey.pfx' -KeyFilePassword $securepfxpwd
    ```
* Bring your own key (BYOK).<br>
    ```
        $key = Add-AzureKeyVaultKey -VaultName 'ContosoKeyVaultHSM' -Name 'ContosoFirstHSMKey' -KeyFilePath 'c:\ITByok.byok' -Destination 'HSM'
    ```
* Generate a key.<br>
    ```
        $key = Add-AzureKeyVaultKey -VaultName 'ContosoKeyVault' -Name 'ContosoFirstKey' -Destination 'Software'
    ```
* Backup a key using Key Vault backup capability and then restore a backed-up key.<br>
    ```
        Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
        Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
    ```
* Overview of basic commands for Key Vault<br>
[Key Vault Getting Started Guide](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
**Troublshooting**

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?<br>
[Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)
* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?<br>
[Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**
[Backup key with Key Vault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey?view=azurermps-4.3.1)<br>
[Restore key with Key Vault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey?view=azurermps-4.3.1)<br>
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[Using Soft-Delete with Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)<br>
[Using Soft-Delete with Key Vault with CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-cli)<br>
[Set up key vault with end-to-end key rotation and auditing](https://docs.microsoft.com/azure/key-vault/key-vault-key-rotation-log-monitoring)<br>