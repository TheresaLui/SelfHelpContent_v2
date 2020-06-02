<properties
	pageTitle="Gremlin partitioning"
	description="Explanation of partitioning of graph across document collection"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="olignat"
	ms.author="olignat"
	selfHelpType="generic"
	supportTopicIds="32675634"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-gremlin-partitioning"
	displayOrder="183"
	category="Gremlin (Graph)"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Gremlin - Partitioning
Most users are able to resolve their Gremlin Partitioning issue using the steps below. 

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

[Partitioning and horizontal scaling in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data)
<br>This article explains physical and logical partitions in Azure Cosmos DB. It also discusses best practices for scaling and partitioning.  

[Using a partitioned graph in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/graph-partitioning)
<br>Partitioning is required if the container is expected to store more than 10 GB in size or if you want to allocate more than 10,000 request units per second (RUs). The same general principles from the Azure Cosmos DB partitioning mechanism apply with a few graph-specific optimizations described in this article.  

