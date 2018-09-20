<properties
	pageTitle="SQL query"
  	description="SQL query"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="rnagpal"
	displayOrder="107"
	selfHelpType="resource"
	supportTopicIds="32597554"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# SQL queries for Azure Cosmos DB

Common reasons for slow queries are (a) low provisioned throughput (b) low parallelism (for cross partition queries) and (c) using operators that can only by served via scans like CONTAINS. When possible, write queries to use a filter on partition key.
Please refer to documents below on how to measure RUs per query, and get execution statistics to tune your queries.

## **Recommended documents**

* [Query Azure Cosmos DB data with SQL queries](https://docs.microsoft.com/azure/cosmos-db/sql-api-sql-query)
* [Tuning query performance with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/sql-api-sql-query-metrics)
* [How does Azure Cosmos DB index data](https://docs.microsoft.com/azure/cosmos-db/indexing-policies)
