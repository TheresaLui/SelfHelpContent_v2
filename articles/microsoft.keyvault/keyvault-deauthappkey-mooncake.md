<properties
	pageTitle="Authorizing and Deauthorizing Applications to Use Keys"
	description="Authorizing and Deauthorizing Applications to Use Keys"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="7"
	selfHelpType="resource"
	supportTopicIds="32375284"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="MoonCake"
	articleId="a6ae6509-9a17-4c40-94d7-7c7d580ed8db"
/>

# Authorizing and Deauthorizing Applications to Use Keys
## **Recommended steps**

* Authorizing Applications to Use Keys
* Authorize an application to use a key or secret. Assume for this example that the service principal name (spn) is "yourSPN" and that the user principal name is "yourUPN".
    ```
        az keyvault set-policy --name 'ContosoKeyVault' --spn yourSPN --key-permissions decrypt sign
        az keyvault set-policy --name 'ContosoKeyVault' --upn yourUPN --secret-permissions get
    ```
* Deauthorizing application to use keys.
    ``` 
        az keyvault delete-policy --name 'ContosoKeyVault' --upn yourUPN
    ```
**Troublshooting**

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?

    [Grant permission to many applications to access a key vault](https://docs.azure.cn/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Azure CLI 2.0 Documentation](https://docs.microsoft.com/cli/azure/keyvault?view=azure-cli-latest#az_keyvault_delete_policy)
* [Using Soft-Delete with Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-soft-delete-powershell)
* [Using Soft-Delete with Key Vault with CLI 2.0](https://docs.azure.cn/key-vault/key-vault-soft-delete-cli)
* [Using Soft-Delete with Key Vault](https://docs.azure.cn/key-vault/key-vault-ovw-soft-delete)
* [Using Managed Storage Account Keys](https://docs.azure.cn/zh-cn/key-vault/key-vault-ovw-storage-keys)