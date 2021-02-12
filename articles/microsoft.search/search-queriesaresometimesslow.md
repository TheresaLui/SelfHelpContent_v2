<properties
	pageTitle="Performance and Throughput/Search queries are sometimes slow"
	description="Search queries are sometimes slow"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	ms.author="mcarter"
	selfHelpType="resource"
	displayOrder="31"
	supportTopicIds="32681385"
	resourceTags=""
	productPesIds="15568"
	articleId="search-queriesaresometimesslow"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Search queries are sometimes slow

## **Recommended Steps**

* If your search service is not under consistent load, please be aware that query latency may periodically be much slower than desired. This is because the service can become "cold" and may take additional time to load caches to serve up your response.  Azure Cognitive Search is optimized for performance under load.
* When there is a spike in request volume at the search service level, either indexing or query, the latency of all requests may also increase.  In most cases, the recommendation here would be to slow down updates to the index and make more room for search queries, since an actual end user is usually waiting for their search results and indexing operations are typically asynchronous.
* During periods of peak request traffic, you may see responses with an HTTP 503 code. This means your service is throttling requests because you have reached the request volume your service can handle.  During throttling, query and indexing latency will increase. You can avoid throttling by scaling in the number of *replicas* in your search service.

## **Recommended Documents**

* [Scale for performance on Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-performance-optimization)<br>
* [Adjust capacity in Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-capacity-planning)<br>