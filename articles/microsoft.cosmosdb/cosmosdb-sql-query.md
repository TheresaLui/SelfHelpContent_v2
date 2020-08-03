<properties
    pageTitle="SQL query"
    description="SQL query"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="ginamr"
    ms.author="girobins"
    selfHelpType="generic"
    supportTopicIds="32636818,32636821,32688845,32741534"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-sql-query"
    displayOrder="65"
    category="Core (SQL)"
    ownershipId="AzureData_AzureCosmosDB"
/>

# SQL queries for Azure Cosmos DB

## **Recommended Steps**

For optimal query performance, follow the steps from the [Troubleshoot Query Performance](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-query-performance) article.

The most common issues and workarounds are detailed below.

**Read all query pages**  

If you think you are not getting all the results, make sure to drain the continuation fully. In other words, make sure you have progressed through all query pages.

You can progress through all query pages by doing either of the following patterns:

- Continue processing while query has more results
- Continue processing results while continuation is not empty

Here are code samples for query pagination in the latest Azure Cosmos DB SDKs:

- [.NET SDK](https://github.com/Azure/azure-cosmos-dotnet-v3/blob/master/Microsoft.Azure.Cosmos.Samples/Usage/Queries/Program.cs#L280-L286)
- [Java SDK](https://github.com/Azure-Samples/azure-cosmos-java-sql-api-samples/blob/master/src/main/java/com/azure/cosmos/examples/documentcrud/sync/DocumentCRUDQuickstart.java#L162-L176)
- [Node.js SDK](https://github.com/Azure/azure-sdk-for-js/blob/83fcc44a23ad771128d6e0f49043656b3d1df990/sdk/cosmosdb/cosmos/samples/IndexManagement.ts#L128-L140)
- [Python SDK](https://github.com/Azure/azure-sdk-for-python/blob/master/sdk/cosmos/azure-cosmos/samples/examples.py#L89)

Learn more about [pagination in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/sql-query-pagination).

**Tune Query Feed Options Parameters**  

Query performance can be tuned via the request's [Feed Options](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.feedoptions?view=azure-dotnet) Parameters. Try setting the below options:

  * Set *MaxDegreeOfParallelism* to -1 first and then compare performance across different values
  * Set *MaxBufferedItemCount* to -1 first and then compare performance across different values
  * Set *MaxItemCount* to -1

When comparing performance of different values, try values such as 2, 4, 8, 16, and others.

**Optimize ORDER BY queries with a composite index**  

Almost all ORDER BY queries with a filter can be optimized with a composite index.

For example, consider the below SQL query:

`SELECT * FROM c WHERE c.name = "John" ORDER BY c.timestamp asc`

This query has a filter on `name` and also has an `ORDER BY` clause. If you create a composite index for `(name asc, timestamp asc)` and `name` is included in the `ORDER BY` clause, the RU charge will decrease **significantly**.

For additional uses for composite indexes see [Composite Indexes](https://docs.microsoft.com/azure/cosmos-db/index-policy#composite-indexes).

**Choose system functions that utilize index**  

Not all system functions utilize the index.

Here is the list of the most commonly used string functions that don't utilize the index:
    
- [LOWER(<str_expr>)](https://docs.microsoft.com/azure/cosmos-db/sql-query-lower)
  - Consider using case-insensitive [CONTAINS](https://docs.microsoft.com/azure/cosmos-db/sql-query-contains), [STARTSWITH](https://docs.microsoft.com/azure/cosmos-db/sql-query-startswith), or [STRINGEQUALS](https://docs.microsoft.com/azure/cosmos-db/sql-query-stringequals) instead.
- [UPPER(<str_expr>)](https://docs.microsoft.com/azure/cosmos-db/sql-query-upper)
  - Consider using case-insensitive [CONTAINS](https://docs.microsoft.com/azure/cosmos-db/sql-query-contains), [STARTSWITH](https://docs.microsoft.com/azure/cosmos-db/sql-query-startswith), or [STRINGEQUALS](https://docs.microsoft.com/azure/cosmos-db/sql-query-stringequals) instead.
- [Most mathematical system functions](https://docs.microsoft.com/azure/cosmos-db/sql-query-mathematical-functions)
  - Avoid using mathematical system functions in the `WHERE` clause of your query, if possible.

For more system function details see [System Functions](https://docs.microsoft.com/azure/cosmos-db/sql-query-system-functions). You can navigate to each individual system function's page in the documentation to understand how it uses the index.

## **Recommended Documents**

Please refer to documents below on how to get execution statistics and tune your queries:

* [Troubleshoot Query Performance](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-query-performance)
* [Performance tips for .NET SDK](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
* [Performance tips for Java SDK](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java-sdk-v4-sql?tabs=api-async)
* [Indexing in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/index-policy)
