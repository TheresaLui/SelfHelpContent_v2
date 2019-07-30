<properties
	pageTitle="Indexing Policy"
	description="Indexing Policy"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="ginamr"
	ms.author="girobins"
	selfHelpType="resource"
	supportTopicIds="32636795"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="MoonCake"
	articleId="cosmosdb-indexing-policy"
	displayOrder="35"
	category="Core (SQL)"
/>

# Indexing Policy in Azure Cosmos DB

## **Recommended Steps**

To verify that the current [Indexing Policy](https://docs.azure.cn/cosmos-db/how-to-manage-indexing-policy) is optimal:

1. Ensure all JSON paths used in queries are included in the index policy for faster reads
2. Exclude paths not used in queries for more performant writes

## **Recommended Documents**

For more on Indexing Policies and query performance tuning, refer to the documents below:

* [Indexing Policies](https://docs.azure.cn/cosmos-db/indexing-policies)
* [How To Manage Indexing Policy](https://docs.azure.cn/cosmos-db/how-to-manage-indexing-policy)
* [Tuning query performance with Azure Cosmos DB](https://docs.azure.cn/cosmos-db/sql-api-sql-query-metrics)
* [Get SQL query execution metrics using .NET SDK](https://docs.azure.cn/cosmos-db/profile-sql-api-query)
