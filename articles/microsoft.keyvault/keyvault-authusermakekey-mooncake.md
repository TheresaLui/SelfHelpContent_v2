<properties
	pageTitle="Authorizing Users to Create Keys"
	description="Authorizing Users to Create Keys"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="optional"
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="keyvault-authusermakekey-mooncake"
/>

# How to Authorizing Users to Create Keys
## **Recommended Steps**

* Authorizing Users to Create Keys
* You need to [Register the application in Azure Active Directory](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)
* Then, authorize the Application to use secrets and keys.

**Troubleshooting**

* Are you not sure how to create a key vault? 
[Creating and Managing Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-overview)
> Having problems authenticating to your key vault?
>* Currently, the new feature Managed Service Identity (MSI) is the easiest way to authenticate. Managed Service Identity (MSI) allows you to automatically provision AAD Identities. For further details please see the following link to the sample using [Key Vault with MSI in an application in .NET](https://github.com/Azure-Samples/app-service-msi-keyvault-dotnet/) and related [MSI with App Service and Functions tutorial](https://docs.azure.cn/app-service/overview-managed-identity).

## **Recommended Documents**

* [Creating and Managing Key Vault with Azure CLI 2.0](https://docs.azure.cn/key-vault/key-vault-manage-with-cli2)
* [Creating and Managing Key Vault with PowerShell](https://docs.azure.cn/key-vault/key-vault-get-started)
* [Using Azure Key Vault from a Web Application](https://docs.azure.cn/key-vault/key-vault-use-from-web-application)
* [Key Vault Developer's Guide](https://docs.azure.cn/key-vault/key-vault-developers-guide)
* [Azure Code Samples](https://azure.microsoft.com/resources/samples/?service=key-vault&sort=0)