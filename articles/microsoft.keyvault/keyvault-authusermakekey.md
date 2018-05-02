<properties
	pageTitle="Authorizing Users to Create Keys"
	description="Authorizing Users to Create Keys"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	displayOrder="14"
	selfHelpType="resource"
	supportTopicIds="32375285"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="public"
/>

# How to Authorizing Users to Create Keys
## **Recommended Steps**

* Authorizing Users to Create Keys<br>
* You need to [Register the application in Azure Active Directory](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)
* Then, authorize the Application to use secrets and keys.<br>

**Troublshooting**

* Are you not sure how to create a key vault? 
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
> Having problems authenticating to your key vault?<br>
>* Currently, the new feature Managed Service Identity (MSI) is the easiest way to authenticate. Managed Service Identity (MSI) allows you to automatically provision AAD Identities. For further details please see the following link to the sample using [Key Vault with MSI in an application in .NET](https://github.com/Azure-Samples/app-service-msi-keyvault-dotnet/) and related [MSI with App Service and Functions tutorial](https://docs.microsoft.com/azure/app-service/app-service-managed-service-identity).<br> 

## **Recommended Documents**
[Creating and Managing Key Vault with Azure CLI 2.0](https://docs.microsoft.com/azure/key-vault/key-vault-manage-with-cli2)<br>
[Creating and Managing Key Vault with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-get-started)<br>
[Using Azure Key Vault from a Web Application](https://docs.microsoft.com/azure/key-vault/key-vault-use-from-web-application)<br>
[Key Vault Developer's Guide](https://docs.microsoft.com/azure/key-vault/key-vault-developers-guide)<br>
[Azure Code Samples](https://azure.microsoft.com/resources/samples/?service=key-vault&sort=0)<br>