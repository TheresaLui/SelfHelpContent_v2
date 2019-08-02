<properties
	pageTitle="Importing Existing Keys Into Key Vault"
	description="Importing Existing Keys Into Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds="32375293"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="MoonCake"
	articleId="917e26d0-971a-44b3-9c12-da53dacc5c4c"
/>

# How to Import Existing Keys into a Key Vault
## **Recommended Steps**

* Before importing a HSM-protected key to key vault you will need to download the BYOK toolset. Please note that is feature is available on Windows only
* The link above shows you how to generate a key using Thales generatekey program and transfer your key to your key vault.
* Import key into a key vault.
    ```
        $key = Add-AzureKeyVaultKey -VaultName 'ContosoKeyVault' -Name 'ContosoFirstKey' -KeyFilePath 'c:\softkey.pfx' -KeyFilePassword $securepfxpwd
    ```
* Bring your own key (BYOK).
    ```
        $key = Add-AzureKeyVaultKey -VaultName 'ContosoKeyVaultHSM' -Name 'ContosoFirstHSMKey' -KeyFilePath 'c:\ITByok.byok' -Destination 'HSM'
    ```
* Backup a key using Key Vault backup capability and then restore a backed-up key.
    ```
        Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
        Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
    ```

**Troublshooting**

* How to Setup a Key Vault for HSM-protected Keys?
* There are two different types of Key Vaults: "Premium" and "Standard". One example of a scenario where you would create a "Premium" vault would be if you have a vault subscription that supports creation of HSM-protected keys and you want to create HSM-protected keys.

## **Recommended Documents**

* [Creating and Managing Key Vault with Azure CLI 2.0](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)
* [Creating and Managing Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-get-started)