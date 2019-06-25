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
	cloudEnvironments="public"
	articleId="cosmosdb-gremlin-performance"
/>
# Gremlin - Performance

When gremlin traversal latency or cost in RU/s does not match expectations there is a custom Cosmos DB Gremlin step to gain insight.

```
g.V('mary').out().executionProfile()
```

Response of traversal will contain diagnostic information about every physical operator invilved in traversal.

**Property**	| **Explanation**
--- | ---
***totalTime***  | Total amount of time, in milliseconds, traversal took on the server side. If this time is significantly lower than observed latency on the client side it is likely there is a client-side contention
***annotations.percentTime*** | Relative fraction of time spent in a given physical operator. To reduce performance it is recommended to focus on reduction in time on heaviest operators. Time can be reduce by applying more predicates or rewriting traversal.
***storeOps.fanoutFactor*** | Number of partitions Gremlin engine touched during physical operator execution. To improve performance it is recommended to reduce this number.
***storeOps.size*** | Size of data in bytes retrieved by Gremlin engine.

Consder physical characteristics of Cosmos DB and Azure infrastructure when assessing impact of each physical operator.

**Resource** | **Value** | **Explanation**
--- | --- | ---
***Network latency between compute and storage***  | **1-2 milliseconds** | Every time Gremlin query engine needs to reach out to storage layer this cost is paid.
***Storage page size*** | **4 MB** | Data is retrieved in pages, each page requires round-trip between compute and storage layer. Divide ***storeOps.size*** by this size and multiply by network latency to assess time spent in data retrieval phase.

### **Traversal Step Specific Behavior**

1. **.order().by()** and **.group().by()** operators are performed in compute layer. They are heavily impacted by the size of data retrieved from storage layer. To improve performance of this step consider reducing amount of data being retrieved by projecting specific properties. _This behavior will be fixed in near future._
2. **.range()** step has linearly increasing latency and RU/s cost as the window of time moves. When range at offset X is requested, X-1 records are processed but ignored. As such, there is still latency and charge for X-1 records. _This behavior will be fixed in near future._

## **Recommended Documents**

* [How to use the execution profile step to evaluate your Gremlin queries](https://docs.microsoft.com/azure/cosmos-db/graph-execution-profile) 
* [Request Units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)