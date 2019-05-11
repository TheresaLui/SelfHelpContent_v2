<properties
	pageTitle="SQL query"
  	description="SQL query"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="rnagpal"
	ms.author="rnagpal"
	selfHelpType="generic"
	supportTopicIds="32636795, 32636821"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="6f8e4570-de45-428f-9ea9-d45135b5ebf6"
/>

# SQL queries for Azure Cosmos DB

Common reasons for slow queries are:
* Low provisioned throughput.
* Low parallelism (for cross partition queries).
* Using operators that can only by served via scans like CONTAINS. When possible, write queries to use a filter on partition key.

Please refer to documents below on how to measure RUs per query, and get execution statistics to tune your queries:

## **Recommended documents**

* [Query Azure Cosmos DB data with SQL queries](https://docs.microsoft.com/azure/cosmos-db/sql-api-sql-query)
* [Tuning query performance with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/sql-api-sql-query-metrics)
* [How does Azure Cosmos DB index data](https://docs.microsoft.com/azure/cosmos-db/indexing-policies)
