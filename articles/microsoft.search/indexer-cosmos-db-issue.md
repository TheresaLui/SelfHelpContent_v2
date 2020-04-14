<properties
	pageTitle="Issue indexing data from Azure Cosmos DB"
	description="Issue indexing data from Azure Cosmos DB"
	service="microsoft.search"
	resource="searchservices"
	authors="MarkHeff"
	ms.author="maheff"
	selfHelpType="resource"
	supportTopicIds="32681364"
	displayOrder="37"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="indexer-cosmos-db-issue"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue indexing data from Azure Cosmos DB

## **Recommended Steps**

If you are having trouble indexing data from Azure Cosmos DB, you may want to ensure that:

1. The database is populated with data
1. Your connection string is valid and the correct ApiKind is being used based on the API that your Cosmos DB database is using. If you are connecting to the Cosmos DB SQL API, your connection string does not require an ApiKind. For the other APIs, please read the documentation [here](https://docs.microsoft.com/azure/search/search-howto-index-cosmosdb#2---create-a-data-source).
1. The types in your database are supported by Azure Search. See the full list of supported JSON data types [here](https://docs.microsoft.com/azure/search/search-howto-index-cosmosdb#mapping-between-json-data-types-and-azure-cognitive-search-data-types).
1. No firewall is preventing communication between Azure Search and the database

If change detection is not working for you:

1. Confirm that you have specified a [HighWaterMarkChangeDetectionPolicy](https://docs.microsoft.com/azure/search/search-howto-index-cosmosdb#indexing-changed-documents).
1. For a custom query, make sure that the _ts property is projected by the query.

If data deletion detection is not working for you:

1. Confirm the [soft delete](https://docs.microsoft.com/azure/search/search-howto-index-cosmosdb#indexing-deleted-documents) policy is specified.

## **Recommended Documents**

* [How to index Cosmos DB data using an indexer in Azure Cognitive Search](https://docs.microsoft.com/azure/search/search-howto-index-cosmosdb)
* [How to upload documents using indexers from the Azure Portal](https://azure.microsoft.com/documentation/articles/search-import-data-portal/)