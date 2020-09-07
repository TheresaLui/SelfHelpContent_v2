<properties
	pageTitle="Data Migration"
	description="Migrate data to Azure Cosmos DB"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636783, 32636785, 32692543"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-data-migration"
	displayOrder="3"
	category="CosmosDB Backup and Restore"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Migrating data to Azure Cosmos DB
Most users are able to resolve their data migration case using the steps and recommended documents below.


## **Recommended Steps**

You can migrate data to Azure Cosmos DB by using the bulk executor library (to author fast import applications), or the ADF v2 service, or the data migration tool. It is recommended to increase the throughput of your collection for the duration of migration. With the higher throughput, you can avoid rate limiting and migrate data in less time.


### **Unable to connect to Cosmos DB resource using Data Migration Tool**  
The UI based Data Migration tool (dtui.exe) is not currently supported for Table API accounts.  
The command-line Azure Cosmos DB Data Migration tool (dt.exe) can be used to import your existing Azure Table storage data to a Table API GA account, or migrate data from a Table API (preview) account into a Table API GA account. Other sources are not currently supported.  
Please see documentation [Data Migration Tool](https://docs.microsoft.com/azure/cosmos-db/table-import#data-migration-tool).


## **Recommended Documents**

[Migrate terabytes of data into Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/migrate-cosmosdb-data)
<br>Azure Cosmos DB can store terabytes of data. You can perform a large-scale data migration to move your production workload to Azure Cosmos DB. This article describes the challenges involved in moving large-scale data to Azure Cosmos DB and introduces you to the tool that helps with the challenges and migrates data to Azure Cosmos DB. In this case study, the customer used the Cosmos DB SQL API.  

[Copy data to or from Azure Cosmos DB (SQL API) by using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db)
<br>This article outlines how to use Copy Activity in Azure Data Factory to copy data from and to Azure Cosmos DB (SQL API), and use Data Flow to transform data in Azure Cosmos DB (SQL API).  

[Copy data to or from Azure Cosmos DB's API for MongoDB by using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db-mongodb-api)
<br>This article outlines how to use Copy Activity in Azure Data Factory to copy data from and to Azure Cosmos DB's API for MongoDB.

[Azure Cosmos DB bulk executor library overview](https://docs.microsoft.com/azure/cosmos-db/bulk-executor-overview)
<br>The bulk executor library helps you leverage this massive throughput and storage. The bulk executor library allows you to perform bulk operations in Azure Cosmos DB through bulk import and bulk update APIs.   

[Use Data migration tool to migrate your data to Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/import-data)
<br>This tutorial provides instructions on using the Azure Cosmos DB Data Migration tool, which can import data from various sources into Azure Cosmos containers and tables. You can import from JSON files, CSV files, SQL, MongoDB, Azure Table storage, Amazon DynamoDB, and even Azure Cosmos DB SQL API collections. You migrate that data to collections and tables for use with Azure Cosmos DB. The Data Migration tool can also be used when migrating from a single partition collection to a multi-partition collection for the SQL API.  


