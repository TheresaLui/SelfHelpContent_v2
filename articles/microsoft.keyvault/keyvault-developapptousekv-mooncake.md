<properties
	pageTitle="How to Use Key Vault with an Application"
	description="Using key vault with an Application"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32375291"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="MoonCake"
	articleId="a3f8dd78-7c00-441f-93af-e85d80937976"
/>

# Develop an Application to Use Key Vault

## **Recommended Steps**

* Use Key Vault with an Application

    [Using Azure Key Vault from a Web Application](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)
    > [!NOTE]
    >* Currently, the new feature Managed Service Identity (MSI) is the easiest way to authenticate. Managed Service Identity (MSI) allows you to automatically provision AAD Identities. For further details please see the following link to the sample using [Key Vault with MSI in an application in .NET](https://github.com/Azure-Samples/app-service-msi-keyvault-dotnet/) and related [MSI with App Service and Functions tutorial](https://docs.microsoft.com/azure/app-service/app-service-managed-service-identity). 
* Next you need to [Register the application in Azure Active Directory](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)
* Then, authorize the application to use secrets and keys.

    ``` 
		az keyvault set-policy --name 'testVault' --spn yourApplicationClientId --key-permissions decrypt sign
    	az keyvault set-policy --name 'testVault' --spn yourApplicationClientId --secret-permissions get 
	```
**Troublshooting**

* To see how to associate a certificate with an Azure AD application look at [Getting Started with Key Vault for Certificates](https://blogs.technet.microsoft.com/kv/2016/09/26/get-started-with-azure-key-vault-certificates/)
* My subscription was moved from tenant A to tenant B. How do I change the tenant ID for my existing key vault and set correct ACLs for principals in tenant B?

    [Change a key vault tenant ID after a subscription move](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)
* I have several (over 16) applications that need to access a key vault. Since Key Vault only allows 16 access control entries, how can I achieve that?

    [Grant permission to many applications to access a key vault](https://docs.microsoft.com/azure/key-vault/key-vault-group-permissions-for-apps)

## **Recommended Documents**

* [Creating and Managing Key Vault with Azure CLI 2.0](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)
* [Creating and Managing Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-overview)
* [Using Azure Key Vault from a Web Application](https://docs.azure.cn/key-vault/tutorial-net-create-vault-azure-web-app)
* [Key Vault Developer's Guide](https://docs.azure.cn/key-vault/key-vault-developers-guide)
* [Azure Code Samples](https://azure.microsoft.com/resources/samples/?service=key-vault&sort=0)
* [Certificate Based Authentication with Java](https://github.com/Azure-Samples/key-vault-java-certificate-authentication)