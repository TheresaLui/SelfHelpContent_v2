<properties
	pageTitle="Data Migration"
	description="Migrate data to Azure Cosmos DB"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="rnagpal"
	ms.author="rnagpal"
	selfHelpType="generic"
	supportTopicIds="32636783"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public, Mooncake"
	articleId="cosmosdb-data-migration"
	displayOrder="63"
	category="Core (SQL)"
/>

# Migrating data to Azure Cosmos DB

## **Recommended Steps**

You can migrate data to Azure Cosmos DB by using the bulk executor library (to author fast import applications), or the ADF v2 service, or the data migration tool. It is recommended to increase the throughput of your collection for the duration of migration. With the higher throughput, you can avoid rate limiting and migrate data in less time.

## **Recommended Documents**

* [Azure Cosmos DB bulk executor library overview](https://docs.microsoft.com/azure/cosmos-db/bulk-executor-overview)
* [Copy data to or from Azure Cosmos DB using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db?toc=/azure/cosmos-db/toc.json)
* [Use Data migration tool to migrate your data to Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/import-data)
* [Migrate terabytes of data into Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/migrate-cosmosdb-data)
