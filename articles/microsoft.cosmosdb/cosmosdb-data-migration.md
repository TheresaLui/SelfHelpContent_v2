<properties
	pageTitle="Data Migration"
	description="Migrate data to Azure Cosmos DB"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32788297,32788298,32788295"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-data-migration"
	displayOrder="3"
	category="CosmosDB Backup and Restore"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Migrating data to Azure Cosmos DB
Most users are able to resolve their data migration cases using the steps and recommended documents below.


## **Recommended Steps**

You can migrate data to Azure Cosmos DB by using a wide variety of tools. To understand which is the best tool, consider the following factors:

### **Factors affecting the choice of migration tool**

The following factors determine the choice of the migration tool:

* **Online vs. offline migration**: Many migration tools provide a path to do a one-time migration only. This means that the applications accessing the database might experience a period of downtime. Some migration solutions provide a way to do a live migration where there is a replication pipeline set up between the source and the target.
* **Data source**: The existing data can be in various data sources, such as Oracle DB2, DataStax Cassandra, Azure SQL Database, PostgreSQL, and so on. The data can also be in an existing Azure Cosmos DB account, and the intent of migration can be to change the data model or to repartition the data in a container with a different partition key.
* **Azure Cosmos DB API**: For the SQL API in Azure Cosmos DB, there are a variety of tools developed by the Azure Cosmos DB team that aid in the different migration scenarios. All of the other APIs have their own specialized set of tools developed and maintained by the community. Because Azure Cosmos DB supports these APIs at a wire protocol level, these tools should work as-is while migrating data into Azure Cosmos DB too. However, they might require custom handling for throttles because this concept is specific to Azure Cosmos DB.
* **Size of data**: Most migration tools work very well for smaller datasets. When the data set exceeds a few hundred gigabytes, the choice of migration tools is limited. 
* **Expected migration duration**: Migrations can be configured to take place at a slow, incremental pace that consumes less throughput, or to consume the entire throughput provisioned on the target Azure Cosmos DB container and therefore complete the migration more quickly.

### **Examples of migration tool options**

To view the **complete list of options**, see [Cosmos DB migration choices](https://docs.microsoft.com/azure/cosmos-db/cosmosdb-migrationchoices).

Some of the most common options are:

* For SQL API: For offline migrations, [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db) or [the Azure Cosmos DB Spark connector](https://docs.microsoft.com/azure/cosmos-db/spark-connector) are good options. For online migrations, [Striim](https://docs.microsoft.com/azure/cosmos-db/cosmosdb-sql-api-migrate-data-striim) or the [custom migration service](https://github.com/Azure-Samples/azure-cosmosdb-live-data-migrator) are good options.
* For Mongo API: For offline migrations, [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db) or [existing Mongo tools (mongodump, mongorestore)](https://azure.microsoft.com/resources/videos/using-mongodb-tools-with-azure-cosmos-db/) are good options. For online migrations, you can use the [Azure Data Migration service](https://docs.microsoft.com/azure/dms/tutorial-mongodb-cosmos-db-online).
* For Cassandra API: For offline migrations, the [cqlsh COPY command](https://docs.microsoft.com/azure/cosmos-db/cassandra-import-data#migrate-data-using-cqlsh-copy-command) or [copy table with Spark](https://docs.microsoft.com/azure/cosmos-db/cassandra-import-data#migrate-data-using-spark) are good options. For online migrations, [Striim](https://docs.microsoft.com/azure/cosmos-db/cosmosdb-cassandra-api-migrate-data-striim) or [Blitzz](https://docs.microsoft.com/azure/cosmos-db/oracle-migrate-cosmos-db-blitzz) are good options.
* For other APIs: The [Data Migration Tool](https://docs.microsoft.com/azure/cosmos-db/table-import#data-migration-tool) can help migrate data.

## **Recommended Documents**

[View the complete list of migration options available](https://docs.microsoft.com/azure/cosmos-db/cosmosdb-migrationchoices)
<br>This article contains the updated list of migration options.

[Migrate terabytes of data into Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/migrate-cosmosdb-data)
<br>Azure Cosmos DB can store terabytes of data. You can perform a large-scale data migration to move your production workload to Azure Cosmos DB. This article describes the challenges involved in moving large-scale data to Azure Cosmos DB and introduces you to the tool that helps with the challenges and migrates data to Azure Cosmos DB. In this case study, the customer uses the Cosmos DB SQL API.  

[Copy data to or from Azure Cosmos DB (SQL API) by using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db)
<br>This article outlines how to use Copy Activity in Azure Data Factory to copy data from and to Azure Cosmos DB (SQL API), and use Data Flow to transform data in Azure Cosmos DB (SQL API).  

[Copy data to or from Azure Cosmos DB's API for MongoDB by using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db-mongodb-api)
<br>This article outlines how to use Copy Activity in Azure Data Factory to copy data from and to Azure Cosmos DB's API for MongoDB.

[Use Data migration tool to migrate your data to Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/import-data)
<br>This tutorial provides instructions on using the Azure Cosmos DB Data Migration tool, which can import data from various sources into Azure Cosmos containers and tables. You can import from JSON files, CSV files, SQL, MongoDB, Azure Table storage, Amazon DynamoDB, and even Azure Cosmos DB SQL API collections. You migrate that data to collections and tables for use with Azure Cosmos DB. The Data Migration tool can also be used when migrating from a single partition collection to a multi-partition collection for the SQL API.  


