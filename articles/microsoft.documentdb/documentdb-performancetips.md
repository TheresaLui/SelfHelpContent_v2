<properties
	pageTitle="CosmosDB performance tips"
	description="CosmosDB performance tips"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="15"
	selfHelpType="resource"
	supportTopicIds="32597551,32597548"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Performance tips for Azure Cosmos DB

In order to achieve the best performance for applications using Azure Cosmos DB, ensure that you are following below tips:

1. For .NET clients use Direct/TCP connectivity mode and for Java client use Direct/HTTPS connectivity mode for best performance.
2. For .NET clients, call OpenAsync() to avoid increased latency for first few requests due to warm up time.
3. Collocate clients in same Azure region for best latency.
4. For high transaction workloads, increase the number of threads/connection pool size to maximize concurrency of requests.
5. Use singleton client instance for the lifetime of your application.
6. Review your indexing policy and explicitly include paths you need for queries (if possible).
7. Larger documents consume higher RUs for reads and writes, so try to keep your documents small for best performance.

## **Recommended documents**
* [Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
* [Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)
* [Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java)
* [Tuning Query performance](https://docs.microsoft.com/azure/cosmos-db/sql-api-sql-query-metrics)
