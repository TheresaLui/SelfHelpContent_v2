<properties
	pageTitle="Performance and Throughput/Search queries are consistently slow"
	description="Search queries are consistently slow"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	ms.author="mcarter"
	selfHelpType="resource"
	displayOrder="30"
	supportTopicIds="32681384"
	resourceTags=""
	productPesIds="15568"
	articleId="search-queriesareconsistentlyslow"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureSearch_AzureSearch"
/>

# Search queries are consistently slow

If your search service is not under consistent load, please be aware that query latency may periodically be much slower than desired. This is because the service can become "cold" and may take additional time to load caches to serve up your response.  Azure Cognitive Search is optimized for performance under load.

## **Recommended Steps**
If your search queries are consistently slow, here are some recommendations for improving the performance of your queries:

* Reducing the overall size of the response will also reduce the time it takes to send the response to you.  Here are some tactics for reducing the query response size:
  * Reduce the number of fields retrieved.  Especially if a field is not displayed in the search UI.
  * Only retrieve hit highlights for large string fields and not the full content of the field itself, especially if you don't plan on displaying this text in your search UI. 
  * Keep the number of documents retrieved as small as possible.  The default is 5.   
* Simplify the filter criteria for each query.  If you find yourself comparing a single field in a document to one of many possible values, we'd strongly recommend you use the [search.in](https://docs.microsoft.com/azure/search/search-query-odata-search-in-function) function.

* You can also improve query performance by optimizing the definition of your search index:
  * Reduce the number of searchable fields that are enable on the index.  By default, search queries target ALL searchable fields.  You should scope your query down as much as possible to your most important fields. This can improve performance particularly at high data volume, since it reduces the amount of content processed to produce your results.
  * Denormalize or flatten your schema as much as possible.  You should not assume your index schema will be exactly the same as your underlying relational database.  The search index should be optimized for search query performance, which in many cases means copying data from multiple rows in your data source into a single document in the search index to support the filters you'll need.
  * Pre-process your data on the way into your index wherever possible.  For example, if you are looking to find names in a very large string field, you could extract the names at indexing time into a string collection and search that collection for the name later.

* Consider scaling up your service for improved performance:
  * You may be getting all of the performance you can out of your service as currently configured and should consider scaling up.  Adding a partition may improve query performance for queries that match to many documents since your data is divided among more search units and can benefit from some parallel processing.
  * Search units in higher service tiers have more processing power and, as a result, queries may consistently perform better.  This recommendation will incur significant cost and should not be made lightly.  You should test this option heavily to verify performance and consider the [impact on the cost of the service](https://azure.microsoft.com/pricing/details/search/).

## **Recommended Documents**

* [Scale for performance on Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-performance-optimization)<br>
* [Adjust capacity in Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-capacity-planning)<br>