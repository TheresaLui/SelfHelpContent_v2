<properties
	pageTitle="Connectivity/Connection timeouts"
	description="Connectivity/Connection timeouts"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	ms.author="mcarter"
	selfHelpType="generic"
	displayOrder="20"
	supportTopicIds="32681345"
	resourceTags=""
	productPesIds="15568"
	articleId="search-connectiontimeouts"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Connection timeouts

These are some conditions where you may experience a timeout and how to address the issue.

## **Recommended Steps**

* Your search service may be under significant load, both indexing and query, and some requests may also be throttled.  If you experience this behavior consistently, we recommend you add one or more replicas to handle the volume of requests your applications are sending to the service.  [Learn more](https://docs.microsoft.com/azure/search/search-performance-optimization)
* An indexer may timeout when retrieving data from an Azure SQL database.  If you encounter timeout errors, you can use the queryTimeout indexer configuration setting to set the queryTimeout parameter to a value higher than the default 5-minute timeout.  [Learn more](https://docs.microsoft.com/rest/api/searchservice/create-indexer#other-configuration-parameters)

## **Recommended Documents**

* [Scale for performance on Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-performance-optimization)<br>
* [Indexer timeout for Azure SQL databases](https://docs.microsoft.com/rest/api/searchservice/create-indexer#other-configuration-parameters)<br>
