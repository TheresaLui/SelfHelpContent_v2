<properties
	pageTitle="Azure Cosmos DB about long running scale operations"
	description="Azure Cosmos DB about long running scale operations"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="kennthhz"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636798"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-throughput-longscaleoperation"
	displayOrder="242"
	category="Throughput and Scaling"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB about long running scale operations

**How long will my scale operation take?**  

Azure Cosmos DB currently only supports scale up operation. It is typically a long running operation. You can use below table to estimate how long it will take.  

**Note**: Minimum Throughput - **Scale Factor** - *Estimated Duration*

* 400 - **<25** - *<1 minute*
* 400 - **25 < Scale factor < 50** - *6 hours*
* 400 - **50 < Scale factor < 100** - *12 hours*
* 400 - **100 < Scale factor < 200** - *18 hours*
* Less than 400 - **<100** - *<1 minute*
* Less than 400 - **100 < Scale factor < 200** - *6 hours*


## **Recommended Documents**

[Request units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
<br>This article defines how request units (RU) is calculated and steps you need to ensure there are enough resources to meet or exceed the Azure Cosmos DB SLAs.  

[Request unit calculator](https://www.documentdb.com/capacityplanner)
<br>The request unit calculator offers you a quick estimate of the workload cost on Cosmos DB.  

[Set and get throughput for Azure Cosmos DB containers and database](https://docs.microsoft.com/azure/cosmos-db/set-throughput)
<br>This article describes how you can provision throughput at two granularities
* Azure Cosmos containers
* Azure Cosmos databases  

[Partition and scale in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data)
<br>This article explains physical and logical partitions in Azure Cosmos DB. It also discusses best practices for scaling and partitioning.
