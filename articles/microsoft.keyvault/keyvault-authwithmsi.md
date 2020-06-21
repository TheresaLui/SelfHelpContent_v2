<properties
	pageTitle="Azure Key Vault Authentication with Managed Service Identity"
	description="Azure Key Vault Authentication with Managed Service Identity"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="jlichwa"
	ms.author="jalichwa"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32596881"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-authwithmsi"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Azure Key Vault Authentication with Managed Service Identity
## **Recommended Steps**

1. Assign Managed Identity to App or Function
2. Grant Permission to Access your Key Vault
3. Access Key Vault

### **Troubleshooting**

* Unauthorized access, access denied, forbidden, or similar error:

	The principal used doesn't have access to the resource it's trying to access. Grant the App Service's access to a resource.

## **Recommended Documents**

* [Use an App Service Managed Identity to Access Key Vault](https://docs.microsoft.com/azure/key-vault/managed-identity)
* [Use Azure Key Vault with an web app in .NET](https://docs.microsoft.com/azure/key-vault/tutorial-net-create-vault-azure-web-app)
