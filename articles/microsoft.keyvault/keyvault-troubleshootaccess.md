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

* If you have problem with authenticate to key vault in code, use [Authentication SDK](https://azure.github.io/azure-sdk/posts/2020-02-25/defaultazurecredentials.html) 

## **Troubleshooting**

* HTTP 401: Unauthenticated Request - [Troublehooting steps](https://docs.microsoft.com/azure/key-vault/general/rest-error-codes#http-401-unauthenticated-request)

* HTTP 403: Insufficient Permissions - [Troublehooting steps](https://docs.microsoft.com/azure/key-vault/general/rest-error-codes#http-403-insufficient-permissions)

* HTTP 429: Too Many Requests - [Troublehooting steps](https://docs.microsoft.com/azure/key-vault/general/rest-error-codes#http-429-too-many-requests)

## **Recommended Documents**

* Roles that you can use to grant access to Azure resources - [List of Azure Role Definitions](https://docs.microsoft.com/azure/role-based-access-control/role-definitions-list)
