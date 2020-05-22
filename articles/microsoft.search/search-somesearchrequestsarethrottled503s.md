<properties
	pageTitle="Performance and Throughput/Some search requests are throttled (Response code 503)"
	description="Some search requests are throttled (Response code 503)"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	ms.author="mcarter"
	selfHelpType="resource"
	displayOrder="32"
	supportTopicIds="32681387"
	resourceTags=""
	productPesIds="15568"
	articleId="search-somesearchrequestsarethrottled503s"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Some search requests are throttled (Response code 503)

## **Recommended Steps**

When you created your Azure Cognitive Search service, resources were provisioned at the selected service tier that are fixed for the lifetime of your service. It is possible to overload these resources by pushing too many requests at one time, both query and indexing. When this happens, you will see HTTP 503 response codes and latency will increase. This is the intended behavior of the service and completely normal.

The best way to avoid 503s is to scale up your service by adding additional replicas. This will increase the number of total requests your service can handle. (Review the [pricing page](https://azure.microsoft.com/pricing/details/search/) to determine the cost of adding replicas to your search service.)  You should balance the end user impact of 503 responses with the cost. You can start by backing off your indexing requests to favor query over index updates since there is usually a user waiting for their search results. You could also decide to index content only at off hours. It's possible, though, that your query traffic is enough to consume all available resources. In this case, the recommendation would be to add additional replicas.  See the link below for more information.

## **Recommended Documents**

* [Scale for performance on Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-performance-optimization) <br>
* [Adjust capacity in Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-capacity-planning)<br>