<properties
	pageTitle="Gremlin Limits"
	description="Limits on account properties and traversal parameters"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32783707,32783708"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-gremlin-howto"
	displayOrder="191"
	category="Gremlin (Graph)"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Azure Cosmos DB Gremlin How-to
Most users are able to resolve their Gremlin How-to issue using the steps below.

## **Recommended Steps** 
Azure Cosmos DB models vertices and edges as documents and stores them in the same collection. Azure Cosmos DB collections are partitioned. Gremlin stores **vertices** and **outgoing edges** with the same partition key. Edges inherit partitioning key from the source vertex.

* Example of setting partition key on the vertex, if **/pk** is partitioning key on collection: **g.addV('vertexlabel').property('pk', 'pkValue')**
* The following is an example of limiting search of vertices to a single partition key, which demonstrates strategy that instructs Gremlin engine to perform traversal only within a given partition even though there may be vertices matching the criteria in other partitions: **g.withStrategies(PartitionStrategy.build().partitionKey('pk').readPartitions('pkValue').create()).V('V1')**  
* **.outE()** is more efficient than **.inE()** step because outgoing edges are stored with the source vertex. To find incoming edges, Gremlin engine needs to perform a fan-out query across all partitions. If traversal require great performance on incoming edge retrieval step then it is recommended to create two edges *source-to-target* and *target-to-source* and replace *.inE()* with *.outE()*.  

Every traversal hop between vertices connected by an edge requires Gremlin engine to reach into storage layer, even if both vertices are stored in the same partition.


### **Partitioning Best Practices**

A great partitioning key exhibits the following properties:

* Data and load are equally distributed across all partitions
* There are no hot partitions storage or throughput-wise
* Traversal are scoped to a subset of partition and rarely fan-out to all of them  
## **Recommended Documents**

[Limits in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/concepts-limits)
<br>This article provides an overview of the default quotas offered to different resources in the Azure Cosmos DB.  

[Partitioning and horizontal scaling in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data)
<br>This article explains physical and logical partitions in Azure Cosmos DB. It also discusses best practices for scaling and partitioning.  

[Using a partitioned graph in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/graph-partitioning)
<br>Partitioning is required if the container is expected to store more than 10 GB in size or if you want to allocate more than 10,000 request units per second (RUs). The same general principles from the Azure Cosmos DB partitioning mechanism apply with a few graph-specific optimizations described in this article.   

[Azure Cosmos DB Gremlin server response headers and status codes](https://docs.microsoft.com/azure/cosmos-db/gremlin-headers)
<br>This article covers headers that Cosmos DB Gremlin server returns to the caller upon request execution. These headers are useful for troubleshooting request performance, building application that integrates natively with Cosmos DB service and simplifying customer support.  

[Apache TinkerPop Git Repository](https://github.com/apache/tinkerpop)

