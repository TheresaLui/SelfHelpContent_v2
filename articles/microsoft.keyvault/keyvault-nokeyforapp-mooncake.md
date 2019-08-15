<properties
	pageTitle="Application Cannot Obtain or Use a Key"
	description="Application Cannot Obtain or Use a Key"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="18"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="optional"
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="keyvault-nokeyforapp-mooncake"
/>

# Application Cannot Obtain or Use a Key

## **Recommended steps**

* Authorize an application to use a key or secret. Assume for this example that the service principal name (spn) is "yourSPN" and that the user principal name is "yourUPN".

    ```
        az keyvault set-policy --name 'ContosoKeyVault' --spn yourSPN --key-permissions decrypt sign
        az keyvault set-policy --name 'ContosoKeyVault' --upn yourUPN --secret-permissions get
    ```

**Troubleshooting**

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?

    [Change a key vault tenant ID after a subscription move](https://docs.azure.cn/key-vault/key-vault-subscription-move-fix)

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?
    [Grant permission to many applications to access a key vault](https://docs.azure.cn/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Creating and Managing Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-get-started)
* [Create and Manage using CLI 2.0](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)
* [Using Managed Storage Account Keys](https://docs.azure.cn/key-vault/key-vault-ovw-storage-keys)
* [Using Soft-Delete with Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-soft-delete-powershell)
* [Using Soft-Delete with Key Vault with CLI 2.0](https://docs.azure.cn/key-vault/key-vault-soft-delete-cli)
* [Using Soft-Delete with Key Vault](https://docs.azure.cn/key-vault/key-vault-ovw-soft-delete)