<properties
	pageTitle="CosmosDB performance tips"
	description="CosmosDB performance tips"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	ms.author="bharathb"
	selfHelpType="generic"
	supportTopicIds="32636818"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-performancetips"
/>

# Performance tips for Azure Cosmos DB

## **Recommended Steps**

In order to achieve the best performance for applications using Azure Cosmos DB, ensure that you are following below tips:

* For .NET and Async Java, use Direct/TCP connectivity mode
* Collocate clients in same Azure region for better performance
* For high transaction workloads, increase the number of threads/connection pool size to maximize concurrency of requests
* Use singleton client instance for the lifetime of your application
* Review your indexing policy and explicitly include paths you need for queries (if possible)
* Larger documents consume higher RUs for reads and writes, so try to keep your documents small for best performance

## **Recommended Documents**

* [Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
* [Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)
* [Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java)
* [Tuning Query performance](https://docs.microsoft.com/azure/cosmos-db/sql-api-sql-query-metrics)
