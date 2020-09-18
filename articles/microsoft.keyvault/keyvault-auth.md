<properties
	pageTitle="Azure Key Vault Authentication"
	description="Azure Key Vault Authentication"
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
	articleId="keyvault-auth"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Azure Key Vault Authentication

## **Recommended Steps**

Authentication with Key Vault works in conjunction with Azure Active Directory (Azure AD), which is responsible for authenticating the identity of any given security principal.
You can authenticate to Key Vault with managed identity, service principal or user principal.

1. Create identity for service or person

1. Assign access policy or Azure role(RBAC) to Key Vault

1. Authenticate application using Key Vault SDK

### **Troubleshooting**

* Unauthorized access, access denied, forbidden, or similar error:

 The principal used doesn't have access to the resource it's trying to access. Grant the App Service's access to a resource.

* Unable to authenticate using security groups

 Security groups in AAD can take up to 8hr to propagate

## **Recommended Documents**

* [Authenticate to Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/authentication)
* [Grant access to Key Vault with Access Policies](https://docs.microsoft.com/azure/key-vault/general/assign-access-policy-portal)
* [Grant access to Key Vault with Azure Roles](https://docs.microsoft.com/azure/key-vault/general/rbac-guide)
* [Key Vault SDK](https://docs.microsoft.com/azure/key-vault/general/developers-guide#coding-with-key-vault)
* [Authentication Troubleshooting Guide](https://docs.microsoft.com/azure/key-vault/general/troubleshooting-access-issues)
