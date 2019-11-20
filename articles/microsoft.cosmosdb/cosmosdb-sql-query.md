<properties
	pageTitle="SQL query"
	description="SQL query"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="ginamr"
	ms.author="girobins"
	selfHelpType="generic"
	supportTopicIds="32636818, 32636821, 32681012, 32684529, 32688838, 32688839, 32688840, 32688841, 32688842, 32688844, 32688845"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-sql-query"
	displayOrder="65"
	category="Core (SQL)"
/>

# SQL queries for Azure Cosmos DB

##Recommended Steps

For optimal query performance, follow the steps from the [Troubleshoot Query Performance](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-query-performance) article.

The most common issues and workarounds are detailed below. 

**Tune Query Feed Options Parameters**  

Query performance can be tuned via the request's [Feed Options](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.feedoptions?view=azure-dotnet) Parameters. Try setting the below options:

  * Set *MaxDegreeOfParallelism* to -1 first and then compare performance across different values
  * Set *MaxBufferedItemCount* to -1 first and then compare performance across different values 
  * Set *MaxItemCount* to -1

When comparing performance of different values, try values such as 2, 4, 8, 16, and others.

**Read all results from continuations**  

If you think you are not getting all the results, make sure to drain the continuation fully. In other words, keep reading results while the continuation token has more documents to yield.

Fully draining can be achieved with either of the following patterns:

  * Continue processing results while continuation is not empty
  * Continue processing while query has more results

    `
    // using AsDocumentQuery you get access to whether or not the query HasMoreResults  
    // If it does, just call ExecuteNextAsync until there are no more results  
    // No need to supply a continuation token here as the server keeps track of progress  
    var query = client.CreateDocumentQuery<Family>(collectionLink, options).AsDocumentQuery();  
    while (query.HasMoreResults)  
    {  
        foreach (Family family in await query.ExecuteNextAsync())  
        {  
            families.Add(family);  
        }  
    }  
    `

**Choose system functions that utilize index**  

If the expression can be translated into a range of string values, then it can utilize the index; otherwise, it cannot. 

Here is the list of string functions that can utilize the index: 
    
  * STARTSWITH(str_expr, str_expr) 
  * LEFT(str_expr, num_expr) = str_expr 
  * SUBSTRING(str_expr, num_expr, num_expr) = str_expr, but only if first num_expr is 0

For more system function details see [System Functions](https://docs.microsoft.com/azure/cosmos-db/sql-query-system-functions).

**Add composite indexes**  

The following queries can be optimized with a composite index:
 * Queries with a filter as well as an ORDER BY clause
 * Queries with filters on multiple properties
 
 For example, consider the below SQL query:
 
`SELECT * FROM c WHERE c.name = "John" ORDER BY c.timestamp asc`
 
This query has a filter on name and also has an ORDER BY clause. If you create a composite index for (name asc, timestamp asc) and name is included in the ORDER BY clause, the RU charge will decrease significantly.

For more details about composite indexes see [Composite Indexes](https://docs.microsoft.com/azure/cosmos-db/index-policy#composite-indexes).

##Recommended Documents

Please refer to documents below on how to get execution statistics and tune your queries:

[Troubleshoot Query Performance](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-query-performance)
<br>
This article covers how to identify, diagnose, and troubleshoot Azure Cosmos DB SQL query issues. In order to achieve optimal performance for Azure Cosmos DB queries 

[Tuning query performance with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/sql-api-sql-query-metrics)
<br>
This article provides the following information for developers
<br>
- High-level details on how Azure Cosmos DB's SQL query execution works
- Details on query request and response headers, and client SDK options
- Tips and best practices for query performance
- Examples of how to utilize SQL execution statistics to debug query performance  

[Performance tips for .NET SDK](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>
if you're asking "How can I improve my database performance?" consider reading this article  

[Get SQL query execution metrics using .NET SDK](https://docs.microsoft.com/azure/cosmos-db/profile-sql-api-query)
<br>
This article presents how to profile SQL query performance on Azure Cosmos DB. This profiling can be done using QueryMetrics retrieved from the .NET SDK and is detailed here
