<properties
    pageTitle="Expensive queries RCA"
    description="RCA - expensive query operations on collection"
    infoBubbleText="The cosmosdb account has expensive query operations. See details on the right"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="bharathsreenivas"
    ms.author="bharathb"
    articleId="cosmosdb-expensivequeries-rca"
    diagnosticScenario="CosmosDBQueryChargeInsight"
    selfHelpType="rca"
    supportTopicIds="32636761,32636754,32636758,32636759,32636762"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Expensive query operations on collection

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
A large percentage of the total request units (RUs) consumed for your account were due to expensive queries.
<!--/issueDescription-->
We found that one or more queries in your account are consuming an unusually high number of RUs.  You may be able to increase the efficiency of your Azure Cosmos DB queries using the following tips.

## **Recommended Steps**

### Prefer GETs over primary key queries

GET on a single partition key and item key is the most efficient operation in Cosmos DB. If your query uses a partition key and item key filter like `SELECT * FROM c WHERE c.<pk> = 'pk1' and c.id = 'id1'`, then replace the call with a call to GET.

### Prefer queries with a filter on a partition key value

Queries with a filter clause on a single partition key value can be served from a single partition, and therefore consume fewer RUs and have lower latency. For example: `SELECT * FROM c WHERE c.<pk> = 'pk1' AND <filters>`

### Prefer filter operators that can utilize the index

Query with a filter clause on a single partition key and another filter that can be served from the index (=, >=, <=, >, <, and built-in functions like *ARRAY_CONTAINS*, *STARTSWITH*, and geospatial filters).For example: `SELECT * FROM c WHERE c.<pk> = 'pk1' and c.id = 'id1' AND c.timestamp >= '2018-01-01T12:00Z'`. A corollary is limiting/avoiding query without filters (scan) or using filters that cannot use the index (e.g. *ENDSWITH*, *CONTAINS*, !=).

### Prefer paginated queries with limit operators

Queries consume RUs based on the number of items returned. You can limit the RUs consumed by either paging through queries partially (you can resume using the continuation token) or by retrieving a subset of the total result set using the TOP operator, For example: `SELECT TOP 100 * FROM c WHERE <filter>`.

### Tune query using execution metrics

You can profile your top queries to obtain detailed metrics on query execution by passing in the optional *x-ms-documentdb-populatequerymetrics* header (FeedOptions.PopulateQueryMetrics in the .NET SDK). Here is a sample output from *x-ms-documentdb-query-metrics*.

`x-ms-documentdb-query-metrics: totalExecutionTimeInMs=33.67;queryCompileTimeInMs=0.06;queryLogicalPlanBuildTimeInMs=0.02;queryPhysicalPlanBuildTimeInMs=0.10;queryOptimizationTimeInMs=0.00;VMExecutionTimeInMs=32.56;indexLookupTimeInMs=0.36;documentLoadTimeInMs=9.58;systemFunctionExecuteTimeInMs=0.00;userFunctionExecuteTimeInMs=0.00;retrievedDocumentCount=2000;retrievedDocumentSize=1125600;outputDocumentCount=2000;writeOutputTimeInMs=18.10;indexUtilizationRatio=1.00`

Please share the output along with the query to Microsoft Support, and they can help find optimizations to reduce RU consumption.

## **Recommended Documents**

Additionally, you can follow this [link](https://docs.microsoft.com/azure/cosmos-db/sql-api-sql-query-metrics) for general query tuning guidelines.
