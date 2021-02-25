<properties
	pageTitle="Cassandra migration"
	description="Migrate data to Azure Cosmos DB Cassandra API"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32788296"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-cassandra-migration"
	displayOrder="143"
	category="Cassandra"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Migrate data to Azure Cosmos DB Cassandra API
Most users are able to resolve their Cassandra API migration issue using the steps below.

## **Recommended Steps**

### **Unable to Connect Cosmos Cassandra API with Cqlsh**
* Convert the .crt to .cer file [cosmos_sample.js](https://gist.github.com/prashanthmadi/afba93b4871fd8e79f22e13ecf05ecfc)
* Do not deactivate the TLS
* Check your firewall configuration for this service. Do you have **Allow access** from **All networks** or from **Selected networks**? If **Selected networks** is selected, do you have the IP address from which you are attempting to connect from added to the Allow list?

## **Recommended Documents**

[Migrate your data to Azure Cosmos DB Cassandra API account](https://docs.microsoft.com/azure/cosmos-db/cassandra-import-data)
<br>This tutorial covers the following tasks:
* Plan for migration
* Prerequisites for migration
* Migrate data using `cqlsh COPY` command
* Migrate data using Spark  

[Azure Cosmos DB Cassandra API data migration options](https://docs.microsoft.com/azure/cosmos-db/cosmosdb-migrationchoices#azure-cosmos-db-cassandra-api)
<br>Migration type, options, and considerations

[Learning Lab 3 - Migrate Cassandra Workloads to Cosmos DB](https://github.com/MicrosoftLearning/DP-060T00A-Migrating-your-Database-to-Cosmos-DB/blob/master/Labs/Lab%203%20-%20Migrate%20Cassandra%20Workloads%20to%20Cosmos%20DB.md)
<br>In this lab, you will migrate two datasets from Cassandra to Cosmos DB. You will move the data in two ways. First, export the data from Cassandra and use the CQLSH COPY command to import the database into Cosmos DB. Then, you will migrate the data using Spark. Finally verify that migration was successful by running queries against the data held in the Cosmos DB database.
