<properties
	pageTitle="Large (TB+) migrations"
	description="Large (TB+) migrations"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32681009"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-largetbmigrations"
	displayOrder="45"
	category="General Advisory"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Large Scale Migrations  
Most users are able to resolve their Large Scale Migration case using the steps below.

## **Recommended Steps**

You can migrate data to Azure Cosmos DB by using the bulk executor library (to author fast import applications), or the ADF v2 service, or the data migration tool. It is recommended to increase the throughput of your collection for the duration of migration. With the higher throughput, you can avoid rate limiting and migrate data in less time.

### **Is it possible to change a Mongo collection from fixed to unlimited?**  
As of today, for Cosmos DB Mongo API, you need to create an unlimited collection and migrate the data over using [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db-mongodb-api). Ideally *_id* is common and a good choice to have as a shard key.  




## **Recommended Documents**

[Migrate terabytes of data into Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/migrate-cosmosdb-data)
<br>Azure Cosmos DB can store terabytes of data. You can perform a large-scale data migration to move your production workload to Azure Cosmos DB. This article describes the challenges involved in moving large-scale data to Azure Cosmos DB and introduces you to the tool that helps with the challenges and migrates data to Azure Cosmos DB. In this case study, the customer used the Cosmos DB SQL API.  


