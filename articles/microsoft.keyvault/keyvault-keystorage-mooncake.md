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
	cloudEnvironments="MoonCake"
	articleId="921a9821-fa93-4e7f-9e05-98f4d99fc3cc"
/>

# 4 Ways to Store Keys with Key Vault
## **Recommended steps**

* Please make sure you have installed [PowerShell](https://www.powershellgallery.com/packages/AzureRM/4.1.0). Below are 4 methods for storing keys in a key vault.
* Import key into a key vault.
    ```
        $key = Add-AzureKeyVaultKey -VaultName 'ContosoKeyVault' -Name 'ContosoFirstKey' -KeyFilePath 'c:\softkey.pfx' -KeyFilePassword $securepfxpwd
    ```
* Bring your own key (BYOK).
    ```
        $key = Add-AzureKeyVaultKey -VaultName 'ContosoKeyVaultHSM' -Name 'ContosoFirstHSMKey' -KeyFilePath 'c:\ITByok.byok' -Destination 'HSM'
    ```
* Generate a key.
    ```
        $key = Add-AzureKeyVaultKey -VaultName 'ContosoKeyVault' -Name 'ContosoFirstKey' -Destination 'Software'
    ```
* Backup a key using Key Vault backup capability and then restore a backed-up key.
    ```
        Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
        Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
    ```
* Overview of basic commands for Key Vault

    [Key Vault Getting Started Guide](https://docs.azure.cn/key-vault/key-vault-get-started)

**Troublshooting**

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?

    [Change a key vault tenant ID after a subscription move](https://docs.azure.cn/key-vault/key-vault-subscription-move-fix)

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?

    [Grant permission to many applications to access a key vault](https://docs.azure.cn/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Backup key with Key Vault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey?view=azurermps-4.3.1)
* [Restore key with Key Vault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey?view=azurermps-4.3.1)
* [Creating and Managing Key Vault with Azure CLI 2.0](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)
* [Creating and Managing Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-get-started)
* [Using Soft-Delete with Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-soft-delete-powershell)
* [Using Soft-Delete with Key Vault with CLI 2.0](https://docs.azure.cn/key-vault/key-vault-soft-delete-cli)
* [Set up key vault with end-to-end key rotation and auditing](https://docs.azure.cn/key-vault/key-vault-key-rotation-log-monitoring)