<properties
	pageTitle="I need more storage/throughput"
	description="I need more storage/throughput"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="AndrewHoh"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
/>

# I need more storage/throughput

## **Recommended steps**
Try one of the following recommendations best fitting with your current scenario.

* I am using pre-defined performance collections (**S1**, **S2**, or **S3**) and would like to move to user-defined performance to set my storage and throughput options independently.
You can use the Portal to change the pricing tier to **STANDARD** by following these [instructions](https://docs.azure.cn/cosmos-db/performance-levels#changing-performance-levels-using-the-azure-portal)
* I am using single partition collections or pre-defined performance collections and would like to move to partitioned collections.
You can use the DocumentDB Data Migration Tool to migrate the data from the single-partition collection (**S1**, **S2**, **S3**, or **Standard**) to a partitioned collection by following these [instructions](https://docs.azure.cn/cosmos-db/partition-data#_migrating-from-single-partition-to-partitioned-collections)
* I am looking to just increase the throughput of my current collection.
You can use the Portal to change the throughput by following these [instructions](https://docs.azure.cn/cosmos-db/performance-levels#change-throughput)

## **Recommended documents**
[Migrating from single-partition to partitioned collections](https://docs.azure.cn/cosmos-db/partition-data#_migrating-from-single-partition-to-partitioned-collections)<br>
[Modeling data in DocumentDB](https://docs.azure.cn/cosmos-db/modeling-data)<br>
[Performance levels in DocumentDB](https://docs.azure.cn/cosmos-db/performance-levels)
