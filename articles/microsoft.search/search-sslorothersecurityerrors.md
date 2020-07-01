<properties
	pageTitle="Connectivity/SSL or other security errors"
	description="Connectivity/SSL or other security errors"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	ms.author="mcarter"
	selfHelpType="resource"
	displayOrder="18"
	supportTopicIds="32681388"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="search-sslorothersecurityerrors"	
	ownershipId="AzureSearch_AzureSearch"
/>

# SSL or other security errors

## **Recommended Steps**

The security related status codes from the Azure Search REST API are listed below:

* 403 "Forbidden": Confirm that you are passing a valid API key and that the API is allowed to perform the current operation. For example, you may be passing a query key while attempting to update the index definition.
* 502 "Bad Gateway": Ensure the search service endpoint URL in your request is using HTTPS and not HTTP

If you receive a 400 "Bad Request" status code, it may be related to Azure Search encryption using customer-managed keys.  These errors may be returned when you are either creating or updating an index with custom encryption keys enabled and there are issues with the current configuration.  You may also see these error messages when you later execute a request to the Azure Search API and the customer-managed encryption key configuration has changed.

* "Access to the required key vault permissions was denied": The credentials provided are not allowed to access Azure Key Vault or permissions were revoked
* "Could not resolve the key vault uri": The provided Azure Key Vault URI is invalid or the Key Vault does not exist or was deleted
* "The key cannot be found": The requested key does not exist in the Azure Key Vault configured for the index
* "Service does not have a managed identity defined": The index is configured to use a [managed identity](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/overview) to authenticate to Azure Key Vault, but isn't currently enabled for the service or was previously disabled
* "The provided application id is invalid": The index is configured to use an Azure Active Directory id to authenticate to Azure Key Vault, but it is invalid or no longer exists
* "The provided application secret is invalid": The index is configured to use an Azure Active Directory secret to authenticate to Azure Key Vault, but it is invalid or was changed

All client-to-service Azure Cognitive Search interactions require [SSL/TLS 1.2 or higher](https://docs.microsoft.com/security/solving-tls1-problem). To ensure your client applications remain secure, we recommend the TLS version should not be hardcoded.  If your client uses a version of TLS prior to 1.2, you may see the following exception: "The underlying connection was closed: An unexpected error occurred on a send." [Learn more](https://docs.microsoft.com/dotnet/framework/network-programming/tls)

## **Recommended Documents**

* [Security and data privacy in Azure Search](https://docs.microsoft.com/azure/search/search-security-overview#encrypted-transmission-and-storage)<br>
* [HTTP status codes (Azure Search)](https://docs.microsoft.com/rest/api/searchservice/http-status-codes)<br>
* [Azure Search encryption using customer-managed keys in Azure Key Vault](https://docs.microsoft.com/azure/search/search-security-manage-encryption-keys)
