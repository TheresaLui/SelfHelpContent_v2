<properties
	pageTitle="Search Issue querying an index using the REST API"
	description="Issue performing a search query using the Azure Cognitive Search API"
	service="microsoft.search"
	resource="searchservices"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="generic"
	displayOrder="3"
	supportTopicIds="32681371"
	resourceTags=""
	productPesIds="15568"
	articleId="search-query-index-issue"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Search Issue querying an index using the REST API

## **Recommended Steps**

If you were having issues performing a search query using the Azure Cognitive Search REST API, the following outlines the most common reasons for issue:

* Using a Query API key as opposed to the required [Admin API](https://docs.microsoft.com/azure/search/search-security-overview#index-access) Key in the header request
* Forgetting to add the [api-version](https://docs.microsoft.com/azure/search/search-api-versions) to the search request

Often the response 's [HTTP status code](https://docs.microsoft.com/rest/api/searchservice/http-status-codes) and message will give a good indication as to why the call failed

It is also important to understand how Azure Cognitive Search leverages the request to perform the search.  For more details on this, please see [Anatomy of a search request
](https://docs.microsoft.com/azure/search/search-lucene-query-architecture)

## **Recommended Documents**

* [Send your first query](https://docs.microsoft.com/azure/search/search-query-simple-examples)
* [Anatomy of a search request](https://docs.microsoft.com/azure/search/search-lucene-query-architecture)
* [Admin API](https://docs.microsoft.com/azure/search/search-security-overview#index-access) Key in the header request
* [API Version](https://docs.microsoft.com/azure/search/search-api-versions) to the search request
* [HTTP status codes](https://docs.microsoft.com/rest/api/searchservice/http-status-codes)
