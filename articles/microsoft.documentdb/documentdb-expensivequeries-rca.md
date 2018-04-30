<properties
	pageTitle="Expensive queries RCA"
	description="RCA - expensive query operations on collection"
	infoBubbleText="The cosmosdb account has expensive query operations. See details on the right"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathb"
	displayOrder=""
	articleId="query_86D7D1E8-4CEF-40D5-AB7F-B16304CDB097"
  diagnosticScenario="MachineKeyUpdates"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We found a high number of expensive queries for your account
<!--/issueDescription-->
We found that a large percentage of the total RUs consumed for your account were due to expensive queries. 

### Prefer GETs over primary key queries
GET on a single partition key and item key is the most efficient operation in Cosmos DB. If your query uses a partition key and item key filter like `SELECT * FROM c WHERE c.<pk> = 'pk1' and c.id = 'id1'`, then replace the call with a call to GET. 

### Prefer queries with a filter on a partition key value
Query with a filter clause on a single partition key value can be served from a single partition, and therefore consume fewer RUs and have lower latency. For example `SELECT * FROM c WHERE c.<pk> = 'pk1' AND <filters>`

### Prefer filter operators that can utilize the index
Query with a filter clause on a single partition key and another filter that can be served from the index (=, >=, <=, >, <, and built-in functions like *ARRAY_CONTAINS*, *STARTSWITH*, and geospatial filters).For example `SELECT * FROM c WHERE c.<pk> = 'pk1' and c.id = 'id1' AND c.timestamp >= '2018-01-01T12:00Z'`. A corrolary is limiting/avoiding query without filters (scan) or using filters that cannot use the index (e.g. *ENDSWITH*, *CONTAINS*, !=). 

### Prefer paginated queries with limit operators
Query consume RUs based on the number of items returned. You can limit the RUs consumed by either paging through queries partially - you can resume using the continuation token. You can also retrieve a subset of results using the TOP operator, for e.g., `SELECT TOP 100 * FROM c WHERE <filter>`.

### Tune query using execution metrics
You can profile your top queries to obtain detailed metrics on query execution by passing in the optional *x-ms-documentdb-populatequerymetrics* header (FeedOptions.PopulateQueryMetrics in the .NET SDK). Here is a sample output from *x-ms-documentdb-query-metrics*.

`x-ms-documentdb-query-metrics: totalExecutionTimeInMs=33.67;queryCompileTimeInMs=0.06;queryLogicalPlanBuildTimeInMs=0.02;queryPhysicalPlanBuildTimeInMs=0.10;queryOptimizationTimeInMs=0.00;VMExecutionTimeInMs=32.56;indexLookupTimeInMs=0.36;documentLoadTimeInMs=9.58;systemFunctionExecuteTimeInMs=0.00;userFunctionExecuteTimeInMs=0.00;retrievedDocumentCount=2000;retrievedDocumentSize=1125600;outputDocumentCount=2000;writeOutputTimeInMs=18.10;indexUtilizationRatio=1.00`

Please share the output along with the query to Microsoft Support, and they can help find optimizations to reduce RU consummption.

Additionally, you can follow this [link](https://docs.microsoft.com/azure/cosmos-db/sql-api-sql-query-metrics) for general query tuning guidelines.
