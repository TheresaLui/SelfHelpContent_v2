<properties
	pageTitle="Gremlin Limits"
	description="Limits on account properties and traversal parameters"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="olignat"
	ms.author="olignat"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="cosmosdb-gremlin-limits-mooncake"
	displayOrder="29"
	category="Gremlin (Graph)"
/>
# Gremlin - Limits

Cosmos DB Gremlin API is built on top of Cosmos DB infrastructure therefore all Limits in [Azure Cosmos DB](https://docs.azure.cn/cosmos-db/concepts-limits) apply. 

### **Azure Cosmos DB Gremlin limits**

When Gremlin limit is reached, traversal is terminated with ***x-ms-status-code*** = 429 that indicates throttling error.

**Resource**	| **Default limit** | **Explanation**
--- | --- | ---
***Memory Per Request*** | **2 GB** | Maximum memory that a request can consume during processing. Requests which need to do computation over large data sets will consume additional memory, so consider scoping requests to smaller data sets to avoid this limit or consider using OLAP solutions.
***Script Length*** | **64 KB** | Maximum length of a Gremlin traversal script per request.
***Operator Depth*** | **400** |  Total number of unique steps in a traversal. For example, ```g.V().out()``` has operator count of 2 V() and out(), ```g.V('label').repeat(out()).times(100)``` has operator depth of 3 V(), repeat() and out() because ```.times(100)``` is a parameter to ```.repeat()``` operator.
***Degree of parallelism*** | **32** | Maximum number of storage partitions queried in a single request to storage layer. For large graphs with hundreds of partitions this limit will impact traversal execution latency.
***Repeat Limit*** | **32** | Maximum number of iterations a ```.repeat()``` operator can execute. Each iteration of ```.repeat()``` step in most cases performs breadth-first traversal which means that any traversal is limited to at most 32 hops between vertices.
***Traversal Timeout*** | **30 seconds** | Traversal will be terminated when it exceeds this time. Cosmos DB Graph is an OLTP database with vast majority of traversals completing within milliseconds. To perform OLAP queries on Cosmos DB Graph please use [Apache Spark](https://azure.microsoft.com/services/cosmos-db/) with [Graph Data Frames](https://spark.apache.org/docs/latest/sql-programming-guide.html#datasets-and-dataframes) and [Cosmos DB Spark Connector](https://github.com/Azure/azure-cosmosdb-spark).
***Predicate Limit*** | **5** | Count of ```.has()``` or ```.hasNot()``` steps applied on a single vertex or edge. When this limit is hit error surfaced to the application is ```The SQL query exceeded the maximum number of joins. The allowed limit is 5```. This is a temporary inconvenience as team is working to lift this limit. 

## **Recommended Documents**

* [Limits in Azure Cosmos DB](https://docs.azure.cn/cosmos-db/concepts-limits)
