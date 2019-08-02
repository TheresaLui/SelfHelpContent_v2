<properties
	pageTitle="Advisory for Key Vault"
	description="Advisory for Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32452742"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="MoonCake"
	articleId="ee2740e9-e40c-4c32-ab2c-0ec8414b28c3"
/>

# Advisory for Key Vault related tasks

## **Recommended steps**

* How to Create and Manage a Key Vault

    [Key Vault Getting Started Guide in PowerShell](https://docs.azure.cn/key-vault/key-vault-overview)

* Next you need to [Register the application in Azure Active Directory](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)

    Then, authorize the Application to use secrets and keys.

**Troublshooting**

* To see how to associate a certificate with an Azure AD application look at [Getting Started with Key Vault for Certificates](https://blogs.technet.microsoft.com/kv/2016/09/26/get-started-with-azure-key-vault-certificates/)

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?

    [Change a key vault tenant ID after a subscription move](https://docs.azure.cn/key-vault/key-vault-subscription-move-fix)

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?

    [Grant permission to many applications to access a key vault](https://docs.azure.cn/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Creating and Managing Key Vault with Azure CLI 2.0](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)
* [Creating and Managing Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-overview)
* [Using Azure Key Vault from a Web Application](https://docs.azure.cn/key-vault/tutorial-net-create-vault-azure-web-app)
* [Using Soft-Delete with Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-soft-delete-powershell)
* [Using Soft-Delete with Key Vault with CLI 2.0](https://docs.azure.cn/key-vault/key-vault-soft-delete-cli)
* [Using Soft-Delete with Key Vault](https://docs.azure.cn/key-vault/key-vault-ovw-soft-delete)
* [Azure Code Samples](https://azure.microsoft.com/resources/samples/?service=key-vault&sort=0)
* [Key Vault Developer's Guide](https://docs.azure.cn/key-vault/key-vault-developers-guide)
* [Getting Started with Certificates in Key Vault](https://blogs.technet.microsoft.com/kv/2016/09/26/get-started-with-azure-key-vault-certificates/)
* [Set up key vault with end-to-end key rotation and auditing](https://docs.azure.cn/key-vault/key-vault-key-rotation-log-monitoring)
* [Key Vault Storage Account Keys](https://docs.azure.cn/key-vault/key-vault-ovw-storage-keys)
* [Secure Key Vault](https://docs.azure.cn/key-vault/key-vault-secure-your-key-vault)
* [Key Vault Throttling limits](https://docs.azure.cn/key-vault/key-vault-ovw-throttling)