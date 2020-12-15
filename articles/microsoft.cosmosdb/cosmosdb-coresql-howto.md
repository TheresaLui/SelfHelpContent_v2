<properties
    pageTitle="Core SQL How-to"
    description="Core SQL How-to"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32783702"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-coresql-howto"
    displayOrder="75"
    category="Core (SQL)"
    ownershipId="AzureData_AzureCosmosDB"
/>

# "Core (SQL) How-to for Azure Cosmos DB
Most users are able to resolve their Cosmos DB related SQL How-to questions or issues using the steps below.   

## **Recommended Steps**

For optimal query performance, follow the steps from the [Troubleshoot Query Performance](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-query-performance) article.

The most common issues and workarounds are detailed below.

### **Tune Query Feed Options Parameters**  

Query performance can be tuned via the request's [Feed Options](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.feedoptions?view=azure-dotnet) Parameters. Try setting the below options:

  - Set *MaxDegreeOfParallelism* to -1 first and then compare performance across different values
  - Set *MaxBufferedItemCount* to -1 first and then compare performance across different values
  - Set *MaxItemCount* to -1

When comparing performance of different values, try values such as 2, 4, 8, 16, and others.

### **Optimize ORDER BY queries with a composite index**  

Almost all ORDER BY queries with a filter can be optimized with a composite index.

For example, consider the below SQL query:

`SELECT * FROM c WHERE c.name = "John" ORDER BY c.timestamp asc`

This query has a filter on `name` and also has an `ORDER BY` clause. If you create a composite index for `(name asc, timestamp asc)` and `name` is included in the `ORDER BY` clause, the RU charge will decrease **significantly**.

For additional uses for composite indexes see [Composite Indexes](https://docs.microsoft.com/azure/cosmos-db/index-policy#composite-indexes).


## **Recommended Documents**

Please refer to documents below on how to get execution statistics and tune your queries:

[Troubleshoot query issues when using Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-query-performance)
<br>You should use this article as a starting place for troubleshooting slow or expensive queries in the Azure Cosmos DB core (SQL) API.   
You can also use [diagnostics logs](https://docs.microsoft.com/azure/cosmos-db/cosmosdb-monitor-resource-logs) to identify queries that are slow or that consume significant amounts of throughput.  

[Performance tips for .NET SDK](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>Performance tips for Azure Cosmos DB and .NET SDK v2   

[Performance tips for Java SDK](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java-sdk-v4-sql?tabs=api-async)
<br>Performance tips for Azure Cosmos DB Java SDK v4  

[Working with JSON in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/sql-query-working-with-json)
<br>In Azure Cosmos DB's SQL (Core) API, items are stored as JSON. The type system and expressions are restricted to deal only with JSON types.    