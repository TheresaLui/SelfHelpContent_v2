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
We found that a large percentage of the total RUs consumed for your account were due to expensive queries. With Azure Cosmos DB, typically queries perform in the following order from fastest/most efficient to slower/less efficient.

## Reduce RU consumption by preferring GETs
GET on a single partition key and item key is the most efficient operation in Cosmos DB. If your query uses a partition key and item key filter like `SELECT * FROM c WHERE c.<pk> = 'pk1' and c.id = 'id1'`, then replace the call with a call to GET. 

## Prefer queries with a filter on a partition key value
Query with a filter clause on a single partition key value can be served from a single partition, and therefore consume fewer RUs and have lower latency. For example `SELECT * FROM c WHERE c.<pk> = 'pk1' AND <filters>`

## Prefer filter operators that can utilize the index
Query with a filter clause on a single partition key and another filter that can be served from the index (=, >=, <=, >, <, and built-in functions like `ARRAY_CONTAINS`, `STARTSWITH`, and geospatial filters).For example `SELECT * FROM c WHERE c.<pk> = 'pk1' and c.id = 'id1' AND c.timestamp >= '2018-01-01T12:00Z'`. A corrolary is limiting/avoiding query without filters (scan) or using filters that cannot use the index (e.g. ENDSWITH, CONTAINS, !=). 

You can profile your top queries to obtain detailed metrics on query execution by passing in the optional `x-ms-documentdb-populatequerymetrics` header (FeedOptions.PopulateQueryMetrics in the .NET SDK). The value returned in `x-ms-documentdb-query-metrics` has the following key-value pairs meant for advanced troubleshooting of query execution. 

Additionally, you can follow this [link](https://docs.microsoft.com/azure/cosmos-db/performance-tips) for general performance guidelines.
