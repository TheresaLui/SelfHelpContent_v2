<properties
	pageTitle="Search Index/Issue deleting an index"
	description="Issue deleting an Azure Cognitive Search index"
	service="microsoft.search"
	resource="searchservices"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="generic"
	displayOrder="4"
	supportTopicIds="32681362"
	resourceTags=""
	productPesIds="15568"
	articleId="index-delete-issue"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue deleting an index

## **Recommended Steps**

If you were unable to delete an index using an API call rather than directly from the portal, the response's HTTP status code and message will often give a good indication as to why the call failed. Common reasons for this failure include:

* Using a Query API key as opposed to the required Admin API Key
* Incorrectly formed API request 
* The Index was previously deleted
* The service is currently unavailable. You must have 2 or more replicas to ensure an availability SLA.

## **Recommended Documents**

* [Azure Search Delete index via REST](https://docs.microsoft.com/rest/api/searchservice/delete-index) 
* [Azure Search HTTP Response Codes](https://docs.microsoft.com/rest/api/searchservice/http-status-codes)

