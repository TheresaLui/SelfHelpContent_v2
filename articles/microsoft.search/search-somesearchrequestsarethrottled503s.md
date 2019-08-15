<properties
	pageTitle="Performance and Throughput/Some search requests are throttled (Response code 503)"
	description="Performance and Throughput/Some search requests are throttled (Response code 503)"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	selfHelpType="resource"
	supportTopicIds="32681387"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public"
	articleId="search-somesearchrequestsarethrottled503s"
/>

# Some search requests are throttled (Response code 503)

When you created your Azure Search service, resources were provisioned at the appropriate pricing tier (or SKU) that are fixed for the lifetime of the service. It is possible overload these resources by pushing too many search queries at one time. When this happens, you will see HTTP 503 response codes. To avoid a 503 during testing, start with various ranges of search requests to see the differences in latency rates as you add more search requests.Azure Search does not run indexing tasks in the background. If your service handles query and indexing workloads concurrently, take this into account by either introducing indexing jobs into your query tests, or by exploring options for running indexing jobs during off peak hours.

## **Recommended steps

## **Recommended documents**
[Deployment strategies and best practices for optimizing performance on Azure Search](https://docs.microsoft.com/azure/search/search-performance-optimization) <br>
[Scale partitions and replicas for query and indexing workloads in Azure Search](https://docs.microsoft.com/azure/search/search-capacity-planning)
