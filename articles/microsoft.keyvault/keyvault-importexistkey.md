<properties
	pageTitle="Importing Existing Keys Into Key Vault"
	description="Importing Existing Keys Into Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="20"
	selfHelpType="resource"
	supportTopicIds="32375293"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Import Existing Keys into a Key Vault
## **Recommended Steps**

* How to import a key from a HSM<br>
[HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)
* Before importing a HSM-protected key to key vault you will need to download the BYOK toolset. Please note that is feature is available on Windows only<br>
* The link above shows you how to generate a key using Thales generatekey program and transfer your key to your key vault.<br>
* Import key into a key vault.<br>
    ```
        $key = Add-AzureKeyVaultKey -VaultName 'ContosoKeyVault' -Name 'ContosoFirstKey' -KeyFilePath 'c:\softkey.pfx' -KeyFilePassword $securepfxpwd
    ```
* Bring your own key (BYOK).<br>
    ```
        $key = Add-AzureKeyVaultKey -VaultName 'ContosoKeyVaultHSM' -Name 'ContosoFirstHSMKey' -KeyFilePath 'c:\ITByok.byok' -Destination 'HSM'
    ```
* Backup a key using Key Vault backup capability and then restore a backed-up key.<br>
    ```
        Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
        Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
    ```

**Troublshooting**

* How to Setup a Key Vault for HSM-protected Keys?<br>
* There are two different types of Key Vaults: "Premium" and "Standard". One example of a scenario where you would create a "Premium" vault would be if you have a vault subscription that supports creation of HSM-protected keys and you want to create HSM-protected keys.<br>

## **Recommended Documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[How to Generate and Transfer HSM-protected keys for Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-hsm-protected-keys)<br>