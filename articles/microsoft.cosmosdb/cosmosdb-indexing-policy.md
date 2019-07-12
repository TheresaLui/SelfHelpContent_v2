<properties
	pageTitle="Indexing Policy"
	description="Indexing Policy"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="ginamr"
	ms.author="girobins"
	selfHelpType="generic"
	supportTopicIds="32636795"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-indexing-policy"
/>

# Indexing Policy in Azure Cosmos DB

## **Recommended Steps**

To verify that the current [Indexing Policy]((https://docs.microsoft.com/azure/cosmos-db/how-to-manage-indexing-policy)) is optimal:

1. Ensure all JSON paths used in queries are included in the index policy for faster reads.
2. Exclude paths not used in queries for more performant writes.

For more details see [Troubleshoot Query Performance](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-query-performance#check-indexing-policy) article.

## **Recommended Documents**
For more on Indexing Policies and query performance tuning, refer to the documents below:

* [Indexing Policies](https://docs.microsoft.com/azure/cosmos-db/indexing-policies)
* [How To Manage Indexing Policy](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-indexing-policy)
* [Tuning query performance with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/sql-api-sql-query-metrics)
* [Get SQL query execution metrics using .NET SDK](https://docs.microsoft.com/azure/cosmos-db/profile-sql-api-query)