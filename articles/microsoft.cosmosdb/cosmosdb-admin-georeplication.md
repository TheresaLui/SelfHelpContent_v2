<properties
	pageTitle="Geo-replication with Cosmos DB"
	description="Troubleshoot CosmosDB Geo-replication related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636794"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-admin-georeplication"
	displayOrder="22"
	category="Administration"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Testing business continuity during regional failures

Regional outages aren't uncommon, and Azure Cosmos DB makes sure your database is always highly available. [High availability in Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/high-availability#high-availability-with-cosmos-db-in-the-event-of-regional-outages) captures Cosmos DB behavior during an outage, depending on your Cosmos account configuration. 

For FAQ on RTO and RPO, guarantees during regional failures across consistency levels and number of regions, and how to configure your applications for high availability, see [Building highly available applications](https://docs.microsoft.com/azure/cosmos-db/high-availability#building-highly-available-applications).

Customers can achieve an RTO of zero by enabling multiple-region writes (multi-master) on their Cosmos accounts using SQL-API with a small change to the Cosmos connection policy in your applications. To configure multiple-region writes for your account see, [Configure multiple write-regions](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account#configure-multiple-write-regions). For details on changes to your application see, [Configure multi-master in your applications](https://docs.microsoft.com/azure/cosmos-db/how-to-multi-master).

## **Recommended Steps**

* For single-region write accounts, you can test High Availability by [triggering a manual failover](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account#manual-failover)

* For multi-region write accounts, you can test High Availability by [adding and removing a region dynamically](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account#addremove-regions-from-your-database-account)  

### **How does Free Tier discount work if I have an account with multiple regions?**  
In multi-region accounts, the RUs of the database or container are replicated in all regions. For example, if you have a container with 400 RUs and the account is in 3 regions, the total RUs of the account is 1200 RUs. When the discount is applied, you will be billed for 1200 RUs – 400 RUs = 800 RUs per hour.


## **Recommended Documents**

[High availability with Cosmos DB in the event of regional outages](https://docs.microsoft.com/azure/cosmos-db/high-availability#high-availability-with-cosmos-db-in-the-event-of-regional-outages)
<br>Regional outages are not uncommon, and Azure Cosmos DB makes sure your database is always highly available. This article captures Cosmos DB behavior during an outage, depending on your Cosmos account configuration.  

[Azure Cosmos DB Consistency Level Tradeoffs](https://docs.microsoft.com/azure/cosmos-db/consistency-levels-tradeoffs)
<br>Distributed databases that rely on replication for high availability, low latency, or both must make tradeoffs. The tradeoffs are between read consistency vs. availability, latency, and throughput.
<br>This article describes the differences in these trade offs.  

[Multi-region accounts](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account)
<br>This article describes how to manage various tasks on an Azure Cosmos account using the Azure portal, Azure PowerShell, Azure CLI, and Azure Resource Manager templates.  

[Distribute data globally](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
<br>This article describes the Key benefits of global distribution:
* Build global active-active apps
* Highly responsive apps
* Highly available apps
* Maintain business continuity during regional outages
* Scale read and write throughput globally
* Choose from several well-defined consistency models
