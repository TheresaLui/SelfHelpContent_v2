<properties
	pageTitle="Database level throughput"
	description="Database level throughput"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636786"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-Databaselevel"
	displayOrder="243"
	category="Throughput and Scaling"
/>

# Database level throughput

## **Recommended Steps**

### **Throughput distribution in database level offer**

When you provision containers with shared database offering:

- Every 25 containers are grouped into a partition set and the database throughput(D) is shared between the containers in the partition set. If there are up to 25 containers in the database and at any point of time, if you are using only one container, then that container can use a max of (D) throughput.<br>
- For every new container created after 25 containers, a new partition set is created and the database throughput is split between the new partition sets created (that is D/2 for 2 partition sets, D/3 for 3 partition sets). At any point of time, if you are using only one container from the database, it can use a max of (D/2, D/3, D/4 throughput) respectively. Given the reduced throughput, its recommended that you create no more than 25 containers in one database.<br>
- Please note that there is no throughput allocation or RU load balancing or fairness guarantees across collections

**Example**

- If you create a database named (MyDB) with a provisioned throughput of 10K RU/s <br>
- If you provision 25 containers under (MyDB), then all the containers are grouped into a partition set. At any point of time, if you are using only one container from the database, then it can use a maximum of 10K RU/s (D)<br>
- When you provision 26th container, a new partition set is created and the throughput is split equally between both the partition sets. At any point of time, if you are using only one container from the database, it can use a maximum of 5K RU/s (D/2). Because there are two partition sets, the throughput shareability factor is split into D/2. <br>

![throughput visual](https://docs.microsoft.com/azure/cosmos-db/media/set-throughput/database-level-throughput-shareability-factor.png)

### **Migration from Dedicated throughput collection to Shared throughput**

We do not have out of the box support for migration of the dedicated throughput collection to shared throughput and vice-versa. To switch from dedicated throughput mode to shared throughput mode (and vice versa) after the container is created, you have to create a new container and migrate the data to the new container. You can migrate the data by using the ADF or tools based on change feed processor library.<br>

### **Per Collection Minimum RUs**

The minimum throughput on a shared throughput database depends on the total number of containers that you have ever created in a shared throughput database, measured at 100 RUs per container.

## **Recommended Documents**

* [Provision throughput on containers and databases](https://docs.microsoft.com/azure/cosmos-db/set-throughput)
* [How to distribute data globally with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
* [Partition and scale in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data)
