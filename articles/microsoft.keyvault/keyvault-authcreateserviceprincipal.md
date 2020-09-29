<properties
	pageTitle="Azure Key Vault Create Service Principal"
	description="Azure Key Vault Create Service Principal"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="jlichwa"
	ms.author="jalichwa"
	displayOrder="8"
	selfHelpType="generic"
	supportTopicIds="32596883"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-authcreateserviceprincipal2"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Azure Key Vault Create Service Principal
## **Recommended Steps**

* [Create service principal](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal)

### **Troubleshooting**

* Unauthorized access, access denied, forbidden, or similar error: 

	The principal used doesn't have access to the resource it's trying to access. Grant the App Services access to a resource.

## **Recommended Documents**

* [Use an App Service Managed Identity to Access Key Vault](https://docs.microsoft.com/azure/key-vault/managed-identity)
* [Use Azure Key Vault with an web app in .NET](https://docs.microsoft.com/azure/key-vault/tutorial-net-create-vault-azure-web-app)
