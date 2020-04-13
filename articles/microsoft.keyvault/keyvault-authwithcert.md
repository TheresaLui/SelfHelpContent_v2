<properties
	pageTitle="Azure Key Vault Authentication with Certificate"
	description="Azure Key Vault Authentication with Certificate"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="jlichwa"
	ms.author="jalichwa"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32596880"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-authwithcert"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Azure Key Vault Authentication with Certificate
## **Recommended Steps**

1. Create Service Principal with a Certificate
2. Give Service Principal Permission to Access your Key Vault
3. Access Key Vault with Service Principal and Certificate

### **Troubleshooting**

* Unauthorized access, access denied, forbidden, or similar error:

	The principal used doesn't have access to the resource it's trying to access. Grant the App Service's access to a resource.

## **Recommended Documents**

* [Create service principal](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal)
* [Grant access to Key Vault](https://docs.microsoft.com/azure/key-vault/managed-identity#grant-your-app-access-to-key-vault)
* [Certificate-based authentication with Azure AD](https://docs.microsoft.com/azure/cosmos-db/certificate-based-authentication)
