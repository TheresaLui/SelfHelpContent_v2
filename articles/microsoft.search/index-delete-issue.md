<properties
	pageTitle="Search Index/Issue deleting an index"
	description="Issue deleting an Azure Search index"
	service="microsoft.search"
	resource="searchservices"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="generic"
	displayOrder="5"
	supportTopicIds="32681353"
	resourceTags=""
	productPesIds="15568"
	articleId="index-delete-issue"
	cloudEnvironments="public"
/>

# Issue deleting an index

## **Recommended Steps**

The most common reason for an index not being deleted will happen when making the call from the API as opposed to from the portal. If this is the case, it is important to make note of the HTTP response that comes back from the call as this gives the best indication as to why it failed. Common reasons for this include:

* Using a Query API key as opposed to an Admin API Key (which is required for this action)
* Incorrectly formed API request
* The Index was previously deleted
* The service is currently unavailable.  You must have 2 or more replicas to ensure an availability SLA.

## **Recommended Documents**

* [Azure Search Delete index via REST](https://docs.microsoft.com/rest/api/searchservice/delete-index) 
* [Azure Search HTTP Response Codes](https://docs.microsoft.com/rest/api/searchservice/http-status-codes)
