<properties
	pageTitle="Data Migration"
  	description="Data Migration"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="rnagpal"
	displayOrder="109"
	selfHelpType="resource"
	supportTopicIds="32597509"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Migrating data to Azure Cosmos DB

You can migrate data to Azure Cosmos DB by using the bulk executor library (to author fast import applications), or the ADF v2 service, or the data migration tool. It is recommended to increase the throughput of your collection for the duration of migration. With the higher throughput, you can avoid rate limiting and migrate data in less time.

## **Recommended documents**

* [Azure Cosmos DB bulk executor library overview](https://docs.microsoft.com/azure/cosmos-db/bulk-executor-overview)
* [Copy data to or from Azure Cosmos DB using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db?toc=/azure/cosmos-db/toc.json)
* [Use Data migration tool to migrate your data to Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/import-data)
