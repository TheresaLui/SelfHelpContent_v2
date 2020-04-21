<properties
	pageTitle="Portal/Service information displayed in portal is incorrect or out of date"
	description="Why is the information displayed in the portal out of date"
	service="microsoft.search"
	resource="searchservices"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="generic"
	displayOrder="2"
	supportTopicIds="32681386"
	resourceTags=""
	productPesIds="15568"
	articleId="search-portal-information-out-of-date"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Understanding why the information displayed in the portal out of date

## **Recommended Steps**

If you are having issues getting up-to-date information in the portal, here are the most common reasons:

* Document Count:  Data related to document counts are not updated in the portal real-time.  The timeframe for updating the counts can vary up to hours.  It is also important to note that it  takes some time for data to become searchable after documents have been indexed.  If you need to get an accuracte count, the best practice is to use the [Count API](https://docs.microsoft.com/rest/api/searchservice/Count-Documents)
* Metrics: Similar to documents counts, metrics are not updated in the portal real-time.  The API for [service statistics](https://docs.microsoft.com/rest/api/searchservice/get-service-statistics) can be used top retrieve some statistics and metrics on the search service

## **Recommended Documents**

* [Document Count API](https://docs.microsoft.com/rest/api/searchservice/Count-Documents)
* [Search Service statistics](https://docs.microsoft.com/rest/api/searchservice/get-service-statistics)