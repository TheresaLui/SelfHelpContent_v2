<properties
	pageTitle="Geo-replication with Cosmos DB"
	description="Troubleshoot CosmosDB Geo-replication related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="markjbrown"
	ms.author="mjbrown"
	selfHelpType="resource"
	supportTopicIds="32636794"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-admin-georeplication"
	displayOrder="22"
	category="Administration"
/>

# Testing business continuity during regional failures

Regional outages aren't uncommon, and Azure Cosmos DB makes sure your database is always highly available. [High availability in Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/high-availability#high-availability-with-cosmos-db-in-the-event-of-regional-outages) captures Cosmos DB behavior during an outage, depending on your Cosmos account configuration. 

For FAQ on RTO and RPO, guarantees during regional failures across consistency levels and number of regions, and how to configure your applications for high availability, see [Building highly available applications](https://docs.microsoft.com/azure/cosmos-db/high-availability#building-highly-available-applications).

Customers can achieve an RTO of zero by enabling multiple-region writes (multi-master) on their Cosmos accounts using SQL-API with a small change to the Cosmos connection policy in your applications. To configure multiple-region writes for your account see, [Configure multiple write-regions](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account#configure-multiple-write-regions). For details on changes to your application see, [Configure multi-master in your applications](https://docs.microsoft.com/azure/cosmos-db/how-to-multi-master).

## **Recommended Steps**

* For single-region write accounts, you can test HA by triggering a manual failover
* For multi-region write accounts, you can test HA by adding and removing a region dynamically

## **Recommended Documents**

* [High availability with Cosmos DB in the event of regional outages](https://docs.microsoft.com/azure/cosmos-db/high-availability#high-availability-with-cosmos-db-in-the-event-of-regional-outages)
* [RPO and RTO for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/consistency-levels-tradeoffs#rto)
