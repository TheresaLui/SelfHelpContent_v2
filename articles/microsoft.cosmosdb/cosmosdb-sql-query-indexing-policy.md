<properties
    pageTitle="SQL query"
    description="SQL query"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32636821"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-sql-query-indexing"
    displayOrder="71"
    category="Core (SQL)"
    ownershipId="AzureData_AzureCosmosDB"
/>

# SQL queries for Azure Cosmos DB
Most users are able to resolve their Cosmos DB related SQL query and indexing policy questions or issues using the steps below.   

## **Recommended Steps**

### **Choose system functions that utilize index**  

Not all system functions utilize the index.

Here is the list of the most commonly used string functions that do not utilize the index:
    
- [LOWER(<str_expr>)](https://docs.microsoft.com/azure/cosmos-db/sql-query-lower)
  - Consider using case-insensitive [CONTAINS](https://docs.microsoft.com/azure/cosmos-db/sql-query-contains), [STARTSWITH](https://docs.microsoft.com/azure/cosmos-db/sql-query-startswith), or [STRINGEQUALS](https://docs.microsoft.com/azure/cosmos-db/sql-query-stringequals) instead
- [UPPER(<str_expr>)](https://docs.microsoft.com/azure/cosmos-db/sql-query-upper)
  - Consider using case-insensitive [CONTAINS](https://docs.microsoft.com/azure/cosmos-db/sql-query-contains), [STARTSWITH](https://docs.microsoft.com/azure/cosmos-db/sql-query-startswith), or [STRINGEQUALS](https://docs.microsoft.com/azure/cosmos-db/sql-query-stringequals) instead
- [Most mathematical system functions](https://docs.microsoft.com/azure/cosmos-db/sql-query-mathematical-functions)
  - Avoid using mathematical system functions in the *WHERE* clause of your query, if possible.

For more system function details see [System Functions](https://docs.microsoft.com/azure/cosmos-db/sql-query-system-functions). You can navigate to each individual system function page in the documentation to understand how it uses the index.


### **Read all query pages**

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


### **Getting partial results while executing a distinct query from the portal**
This is expected.  The results are getting paginated. You will need to click on `load more` to drain out all the results.   


### **Understand common query syntax errors**

Consider the examples below where the property `order` is a reserved word and the property `price($)` contains a special character:

```
SELECT *
FROM c
WHERE c["order"].orderId = "12345"
```

```
SELECT *
FROM c
WHERE c["order"]["price($)"] > 50
```

The below example shows aliasing with reserved keywords, spaces, and special characters:

```
SELECT
           {"JSON expression with a space": { "state": f.address.state, "city": f.address.city }},
           {"JSON expression with a special character!": { "name": f.id }}
FROM Families f
WHERE f.id = "AndersenFamily"
```

Learn more about [SQL query syntax in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/sql-query-working-with-json)


## **Recommended Documents**

[Troubleshoot query issues when using Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-query-performance)
<br>You should use this article as a starting place for troubleshooting slow or expensive queries in the Azure Cosmos DB core (SQL) API.   
You can also use [diagnostics logs](https://docs.microsoft.com/azure/cosmos-db/cosmosdb-monitor-resource-logs) to identify queries that are slow or that consume significant amounts of throughput.  

[Working with JSON in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/sql-query-working-with-json)
<br>In Azure Cosmos DB's SQL (Core) API, items are stored as JSON. The type system and expressions are restricted to deal only with JSON types.    

[Indexing in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/index-policy)
<br>In Azure Cosmos DB, every container has an indexing policy that dictates how the container's items should be indexed. The default indexing policy for newly created containers indexes every property of every item and enforces range indexes for any string or number. This allows you to get high query performance without having to think about indexing and index management upfront.  
In some situations, you may want to override this automatic behavior to better suit your requirements. You can customize a container's indexing policy by setting its indexing mode, and include or exclude property paths.
