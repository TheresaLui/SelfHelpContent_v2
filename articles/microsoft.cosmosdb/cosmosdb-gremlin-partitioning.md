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
	cloudEnvironments="public"
	articleId="cosmosdb-gremlin-partitioning"
	displayOrder="183"
	category="Gremlin (Graph)"
/>
# Gremlin - Partitioning

Azure Cosmos DB models vertices and edges as documents and stores them in the same collection. Azure Cosmos DB collections are partitioned. Gremlin stores **vertices** and **outgoing edges** with the same partition key. Edges inherit partitioning key from the source vertex.

* Example of setting partition key on the vertex, if **/pk** is partitioning key on collection: `g.addV('vertexlabel').property('pk', 'pkValue')`
* The following is an example of limiting search of vertices to a single partition key, which demonstrates strategy that instructs Gremlin engine to perform traversal only within a given partition even though there may be vertices matching the criteria in other partitions: `g.withStrategies(PartitionStrategy.build().partitionKey('pk').readPartitions('pkValue').create()).V('V1')`

	`.outE()` is more efficient than `.inE()` step because outgoing edges are stored with the source vertex. To find incoming edges, Gremlin engine needs to perform a fan-out query across all partitions. If traversal require great performance on incoming edge retrieval step then it is recommended to create two edges *source-to-target* and *target-to-source* and replace `.inE()` with `.outE()`.

* Every traversal hop between vertices connected by an edge requires Gremlin engine to reach into storage layer, even if both vertices are stored in the same partition.

### Best Practices

A great partitioning key exhibits the following properties:

1. Data and load are equally distributed across all partitions
2. There are no hot partitions storage or throughput-wise
3. Traversal are scoped to a subset of partition and rarely fan-out to all of them

## **Recommended Documents**

* [Partitioning and horizontal scaling in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data) 
* [Using a partitioned graph in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/graph-partitioning)
