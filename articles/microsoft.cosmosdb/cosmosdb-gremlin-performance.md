<properties
	pageTitle="Gremlin performance"
	description="Investigation of gremlin traversal performance"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="olignat"
	ms.author="olignat"
	selfHelpType="generic"
	supportTopicIds="32675635"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-gremlin-performance"
	displayOrder="184"
	category="Gremlin (Graph)"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Gremlin - Performance
Most users are able to resolve their Gremlin Performance issue using the steps below.  


## **Recommended Steps**  


### **Adjacency list resolution** 
Adjacency list resolution is a function of the total number of edges that need to be resolved and limit() optimizations are not applied to adjacency lookup.  

An approach that we often recommend to customers is to use a range filter on the adjacency.
<br>*g.V('center').bothE().has('range_key', gt('a')).has('range_key', gt('b')).inV().limit(100)*
<br>In this example, **range_key** is a property that can be used to subdivide the entire adjacency list of the vertex.  
 
This has two benefits:
* It can resolve a smaller subset of the adjacency list to satisfy the limit() step and the set that is resolved can be deterministic.
* Provides a means to *paging* neighbor results if a larger data set is required. This can be done by issuing multiple queries which take **range_key** slices to input to the query. This will be particularly important if a vertex has 50000+ edges to traverse.  


### **Traversal Latency**

When Gremlin traversal latency or cost in RU/s does not match expectations there is a custom Cosmos DB Gremlin step to gain insight: `g.V('mary').out().executionProfile()`  

Response of traversal will contain diagnostic information about every physical operator involved in traversal.  

**Property**	| **Explanation**
--- | ---
***totalTime***  | Total amount of time, in milliseconds, traversal took on the server side. If this time is significantly lower than observed latency on the client side it is likely there is a client-side contention
***annotations.percentTime*** | Relative fraction of time spent in a given physical operator. To reduce performance it is recommended to focus on reduction in time on heaviest operators. Time can be reduce by applying more predicates or rewriting traversal.
***storeOps.fanoutFactor*** | Number of partitions Gremlin engine touched during physical operator execution. To improve performance it is recommended to reduce this number.
***storeOps.size*** | Size of data in bytes retrieved by Gremlin engine.

Consider physical characteristics of Cosmos DB and Azure infrastructure when assessing impact of each physical operator.  

**Resource** | **Value** | **Explanation**
--- | --- | ---
*Network latency between compute and storage*  | **1-2 milliseconds** | Every time Gremlin query engine needs to reach out to storage layer this cost is paid.
*Storage page size* | **4 MB** | Data is retrieved in pages, each page requires round-trip between compute and storage layer. Divide **storeOps.size** by this size and multiply by network latency to assess time spent in data retrieval phase.

### **Known Traversal Behavior**

* **g.V().count()** traversal may consume a large amount of RU/s if executed against a large graph. Currently this operation is an aggregation function rather than index look-up and, as such, the cost is proportional to the size of graph. To work around please use SQL end-point and execute a query **SELECT VALUE COUNT(1) FROM Node**. It will return the count of edges and vertices in the graph. It is not a strict match for **g.V().count()** but can be used to assess the size of the graph during ingestion.
*  **g.V().drop()** is expensive and may timeout on large graphs. Cosmos DB Graph engine does not support "truncate" semantics for a graph. A quick way to delete entire graph is to drop the graph or collection instead of deleting all vertices and edges. Vertices and edges are deleted one by one, but a collection/graph drop will delete them all in one operation.
* **.order().by()** and **.group().by()** operators are performed in compute layer. They are heavily impacted by the size of data retrieved from storage layer. To improve performance of this step consider reducing amount of data being retrieved by projecting specific properties. 
* **.range()** step has linearly increasing latency and RU/s cost as the window of time moves. When range at offset X is requested, X-1 records are processed but ignored. As such, there is still latency and charge for X-1 records. 


## **Recommended Documents**  

[Request Units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
<br>With Azure Cosmos DB, you pay for the throughput you provision and the storage you consume on an hourly basis. Throughput must be provisioned to ensure that sufficient system resources are available for your Azure Cosmos database at all times. You need enough resources to meet or exceed the Azure Cosmos DB SLAs.  

[Azure Cosmos DB Gremlin limits](https://docs.microsoft.com/azure/cosmos-db/gremlin-limits)
<br>This article provides an overview of the default quotas offered to different resources in the Azure Cosmos DB.  

[How to use the execution profile step to evaluate your Gremlin queries](https://docs.microsoft.com/azure/cosmos-db/graph-execution-profile)
<br>This article provides an overview of how to use the execution profile step for Azure Cosmos DB Gremlin API graph databases. This step provides relevant information for troubleshooting and query optimizations, and it is compatible with any Gremlin query that can be executed against a Cosmos DB Gremlin API account.

