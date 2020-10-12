<properties
	pageTitle="Partitioning"
	description="Partitioning"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636816,32747698"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-partitioning"
	displayOrder="240"
	category="Throughput and Scaling"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Introduction to Partitioning and Scale in Azure Cosmos DB

Azure Cosmos DB will automatically scale the number of physical partitions based on your workload. 

## **Recommended Steps**

### **Throughput distribution in database level offer**

When you provision containers with shared database offering:

- Every 25 containers are grouped into a partition set and the database throughput(D) is shared between the containers in the partition set. If there are up to 25 containers in the database and at any point of time, if you are using only one container, then that container can use a max of (D) throughput.<br>
- For every new container created after 25 containers, a new partition set is created and the database throughput is split between the new partition sets created (that is D/2 for 2 partition sets, D/3 for 3 partition sets). At any point of time, if you are using only one container from the database, it can use a max of (D/2, D/3, D/4 throughput) respectively. Given the reduced throughput, it is recommended that you create no more than 25 containers in one database.<br>
- Please note that there is no throughput allocation or RU load balancing or fairness guarantees across collections

**Example**

- If you create a database named (MyDB) with a provisioned throughput of 10K RU/s <br>
- If you provision 25 containers under (MyDB), then all the containers are grouped into a partition set. At any point of time, if you are using only one container from the database, then it can use a maximum of 10K RU/s (D)<br>
- When you provision 26th container, a new partition set is created and the throughput is split equally between both the partition sets. At any point of time, if you are using only one container from the database, it can use a maximum of 5K RU/s (D/2). Because there are two partition sets, the throughput shareability factor is split into D/2. <br>


### **Is it possible to change a Mongo collection from fixed to unlimited?**  
As of today, for Cosmos DB Mongo API, you need to create an unlimited collection and migrate the data over using [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db-mongodb-api). Ideally *_id* is common and a good choice to have as a shard key.  


### **Unable to find graphs to show the storage distribution across partitions?**  
Select the Metrics from the left pane and select respective database name and collection name from the drop down to retrieve the metrics.



## **Recommended Documents**

To use all provisioned throughput, you must avoid skews by choosing a good partition key. To learn more about partitioning and partition key selection, see links below.

[Partition and scale in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data)
<br>This article explains physical and logical partitions in Azure Cosmos DB. It also discusses best practices for scaling and partitioning.  

[How to distribute data globally with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
<br>To achieve low latency and high availability, instances of these applications need to be deployed in data centers that are close to their users. These applications are typically deployed in multiple data centers and are called globally distributed. Globally distributed applications need a globally distributed database that can transparently replicate the data anywhere in the world to enable the applications to operate on a copy of the data that's close to its users.  
