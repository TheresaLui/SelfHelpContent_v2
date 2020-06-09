<properties
	pageTitle="Search Index/Issue creating an index"
	description="Issue creating an Azure Cognitive Search index"
	service="microsoft.search"
	resource="searchservices"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="generic"
	displayOrder="3"
	supportTopicIds="32681356"
	resourceTags=""
	productPesIds="15568"
	articleId="search-index-create-issue"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue creating an index

## **Recommended Steps**

If you were unable to create an index using an API call rather than directly from the portal, the response's HTTP status code and message will often give a good indication as to why the call failed. 

Common reasons for this failure from an API call include:

* Using a Query API key as opposed to the required Admin API Key
* Incorrectly formed API request 
* The Index was recently deleted and you re-created an index of the same name in a short timeframe (should try again)
* The service is currently unavailable.  You must have 2 or more replicas to ensure an availability SLA.

In the event that the issue happened in the portal, some common reasons include:
* The Index was recently deleted and you re-created an index of the same name in a short timeframe (should try again)
* The service is currently unavailable.  You must have 2 or more replicas to ensure an availability SLA.
* In rare cases, the portal can be in an unstable state and by refreshing the portal and trying again it often will work

## **Recommended Documents**

* [Azure Search Create index via REST](https://docs.microsoft.com/rest/api/searchservice/create-index) 
* [Azure Search HTTP Response Codes](https://docs.microsoft.com/rest/api/searchservice/http-status-codes)

