<properties
	pageTitle="Gremlin Limits"
	description="Limits on account properties and traversal parameters"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="olignat"
	ms.author="olignat"
	selfHelpType="generic"
	supportTopicIds="32636756"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-gremlin-limits"
/>
# Gremlin - Limits

Cosmos DB Gremlin is built on top of Cosmos DB infrastructure therefore all Limits in [Azure Cosmos DB](https://docs.microsoft.com/en-us/azure/cosmos-db/concepts-limits) apply. 

### **Gremlin-specific limits**

When gremlin-specific limit is reached, traversal is terminated with HTTP 429 Throttling error.

**Resource**	| **Default limit** | **Explanation**
--- | --- | ---
***Memory Per Request*** | **2 GB** | This value limits total response size received from storage layer during request processing.
***Script Length*** | **64 KB** | Maximum length of a Gremlin traversal script per request.
***Operator Depth*** | **400** |  Total number of unique steps in a traversal. For example, ```g.V().out()``` has operator count of 2 V() and out(), ```g.V('label').repeat(out()).times(100)``` has operator depth of 3 V(), repeat() and out() because ```.times(100)``` is a parameter to ```.repeat()``` operator.
***Degree of parallelism*** | **32** | Maximum number of storage partitions queried in a single request to storage layer. For large graphs with hundreds of partitions this limit will impact traversal execution latency.
***Repeat Limit*** | **32** | Maximum number of iterations a ```.repeat()``` operator can execute. Each iteration of ```.repeat()``` step in most cases performs breadth-first traversal which means that any traversal is limited to at most 32 hops between vertices.
***Traversal Timeout*** | **30 seconds** | Traversal will be terminated when it exceeds this time. Cosmos DB Graph is an OLTP database with vast majority of traversals completing within milliseconds. To perform OLAP queries on Cosmos DB Graph please use [Apache Spark](https://azure.microsoft.com/en-us/services/cosmos-db/) with [Graph Data Frames](https://spark.apache.org/docs/latest/sql-programming-guide.html#datasets-and-dataframes) and [Cosmos DB Spark Connector](https://github.com/Azure/azure-cosmosdb-spark).
***Predicate Limit*** | 5 | Number of ```.has()``` or ```.hasNot()``` steps applied on a single vertex or edge. When this limit is hit error surfaced to the application is ```The SQL query exceeded the maximum number of joins. The allowed limit is 5```. This is a temporary inconvenience as team is working to lift this limit. 