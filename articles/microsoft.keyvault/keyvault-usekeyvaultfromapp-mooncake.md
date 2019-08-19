<properties
	pageTitle="Configure an Application to Use Keys"
	description="Using key vault from a web application"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="fhokholdMSFT"
	displayOrder="20"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="optional"
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="keyvault-usekeyvaultfromapp-mooncake"
/>

# How Configure an Application to Use Keys
## **Recommended steps**

* Use Key Vault from Web Application

    [Using Azure Key Vault from a Web Application](https://docs.azure.cn/key-vault/key-vault-get-started)
    > [!NOTE]
    >* Currently, the new feature Managed Service Identity (MSI) is the easiest way to authenticate. Managed Service Identity (MSI) allows you to automatically provision AAD Identities. For further details please see the following link to the sample using [Key Vault with MSI in an application in .NET](https://github.com/Azure-Samples/app-service-msi-keyvault-dotnet/) and related [MSI with App Service and Functions tutorial](https://docs.azure.cn/app-service/overview-managed-identity). 

* Next you need to [Register the application in Azure Active Directory](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)

    Then, authorize the Application to use secrets and keys.

**Troubleshooting**

* To see how to associate a certificate with an Azure AD application look at [Getting Started with Key Vault for Certificates](https://blogs.technet.microsoft.com/kv/2016/09/26/get-started-with-azure-key-vault-certificates/)

* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?

    [Change a key vault tenant ID after a subscription move](https://docs.azure.cn/key-vault/key-vault-subscription-move-fix)

* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?

    [Grant permission to many applications to access a key vault](https://docs.azure.cn/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Creating and Managing Key Vault with Azure CLI 2.0](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)
* [Creating and Managing Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-get-started)
* [Using Azure Key Vault from a Web Application](https://docs.azure.cn/key-vault/key-vault-use-from-web-application)
* [Managed Storage Account Keys](https://docs.azure.cn/key-vault/key-vault-ovw-storage-keys)