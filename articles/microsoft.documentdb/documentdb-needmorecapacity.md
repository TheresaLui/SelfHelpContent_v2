<properties
	pageTitle="I need more storage/throughput"
	description="I need more storage/throughput"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="AndrewHoh"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32597546"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# I need more storage/throughput

## **Recommended steps**
Try one of the following recommendations best fitting with your current scenario.

* If you are using a single partition collections or pre-defined performance collections and would like to move to a partitioned collection, you can use the DocumentDB Data Migration Tool to migrate the data from the single-partition collection to a partitioned collection by following these [instructions](https://azure.microsoft.com/documentation/articles/documentdb-partition-data/#_migrating-from-single-partition-to-partitioned-collections)
* If you are looking to just increase the throughput of my current collection, you can use the Portal or SDK to change the throughput by following these [instructions](https://azure.microsoft.com/documentation/articles/documentdb-performance-levels/#change-throughput)

## **Recommended documents**
[Migrating from single-partition to partitioned collections](https://azure.microsoft.com/documentation/articles/documentdb-partition-data/#_migrating-from-single-partition-to-partitioned-collections)<br>
[Modeling data in DocumentDB](https://azure.microsoft.com/documentation/articles/documentdb-modeling-data/)<br>
