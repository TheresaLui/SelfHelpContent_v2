<properties
	pageTitle="Performance and Throughput/Indexing throughput is lower than expected"
	description="Indexing throughput is lower than expected"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	ms.author="mcarter"
	selfHelpType="resource"
	displayOrder="33"
	supportTopicIds="32681351"
	resourceTags=""
	productPesIds="15568"
	articleId="search-indexingthroughputislowerthanexpected"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Indexing throughput is lower than expected

## **Recommended Steps**

Here are some general recommendations to improve your indexing throughput:

* Index documents in batches. One of the most common mistakes developers make is sending a request to the server for every single document indexed. This introduces significant additional roundtrips and will reduce your indexing throughput considerably. Send a single, large request to the server for a batch of up to 1000 documents or a total request size of 16MB. In the .NET SDK, you would package your data into an `IndexBatch` object, which encapsulates a collection of `IndexAction` objects, each of which contains the document and a property that tells indicates what action to perform on that document. For a code example, see the [C# Quickstart](https://docs.microsoft.com/azure/search/search-get-started-dotnet#2---load-documents).

* Ingest data in parallel as much as possible. When using an indexer, partitioning data into smaller individual data sources enables parallel processing. You can break up your data into smaller sets, such as into multiple containers in Azure Blob Storage, and then create corresponding, multiple data source objects in Azure Cognitive Search that can be indexed in parallel. If you are using the REST API to index documents, your indexing client should use multiple threads for optimal performance. You have reached the maximum indexing throughput your service can handle when you start seeing 503 response codes from the API. For a code example of parallel processing, see this [article](https://docs.microsoft.com/dotnet/standard/parallel-programming/how-to-write-a-simple-parallel-foreach-loop).

* Index content during quiet hours. Remember that query and indexing traffic pull from the same resource pool. You should avoid indexing many documents in the middle of the day, when query traffic is at its peak. Save these operations for later in the day, if possible, when there will be more resources available for indexing. 

* Scale up your service by adding partitions. This typically improves performance since data is distributed evenly among each partition.  The more partitions you have, the less data is on each search unit and each document may be indexed faster. (Review the [pricing page](https://azure.microsoft.com/pricing/details/search/) to determine the cost of adding partitions to your search service.)  You would most likely want to do this when you are performing an initial data load and you can always scale back down to a lower number of partitions once the operation is complete. 

* Understand the impact each skill in your skillset has on your indexing throughput. If you are using skillsets in your indexer, they introduce additional processing demands to your indexing pipeline. Each skill may perform enrichments that add significant value to your data and functionality to your search application, but they will also have a negative impact on indexing throughput. When writing your custom skill, make sure your API can handle batches of input records and then produce a single batched response. In the code for your skill, you should optimize your code for performance by operating on the input in parallel as much as possible. For a code example, see the [custom skill sample](https://docs.microsoft.com/azure/search/cognitive-search-create-custom-skill-example).

## **Recommended Documents**

* [Data import overview](https://docs.microsoft.com/azure/search/search-what-is-data-import)
* [Indexers in Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-indexer-overview)
* [Scale for performance on Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-performance-optimization)<br>