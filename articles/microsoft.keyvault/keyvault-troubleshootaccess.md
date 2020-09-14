<properties
	pageTitle="Troubleshoot Access to Key Vault"
	description="Troubleshoot Access to Key Vault"
	service="Microsoft.Keyvault"
	resource="vaults"
	authors="fhokholdMSFT"
	ms.author="jalichwa"
	displayOrder="19"
	selfHelpType="generic"
	supportTopicIds="32743816"
	resourceTags="optional"
	productPesIds="15657"
	cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	articleId="keyvault-troubleshootaccess"
	ownershipId="AzureKeyVault_KeyVault"
/>

# Troubleshoot Access to Key Vault

## **Recommended Steps**

* [Answered questions about issues related to access policy in key vault](https://docs.microsoft.com/azure/key-vault/general/troubleshooting-access-issues)

* If you have problem with authenticate to key vault in code, use [Authentication SDK](https://docs.microsoft.com/azure/key-vault/general/developers-guide#coding-with-key-vault) 

### **Troubleshooting**

* HTTP 401: Unauthenticated Request - [Troubleshooting steps](https://docs.microsoft.com/azure/key-vault/general/rest-error-codes#http-401-unauthenticated-request)
* HTTP 403: Insufficient Permissions - [Troubleshooting steps](https://docs.microsoft.com/azure/key-vault/general/rest-error-codes#http-403-insufficient-permissions)
* HTTP 429: Too Many Requests - [Troubleshooting steps](https://docs.microsoft.com/azure/key-vault/general/rest-error-codes#http-429-too-many-requests)

## **Recommended Documents**

* Roles that you can use to grant access to Azure resources - [List of Azure Role Definitions](https://docs.microsoft.com/azure/role-based-access-control/role-definitions-list)
* [Authenticate to Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/authentication)
* [Grant access to Key Vault with Access Policies](https://docs.microsoft.com/azure/key-vault/general/assign-access-policy-portal)
* [Grant access to Key Vault with Azure Roles](https://docs.microsoft.com/azure/key-vault/general/rbac-guide)
* [Key Vault SDK](https://docs.microsoft.com/azure/key-vault/general/developers-guide#coding-with-key-vault)
