<properties
	pageTitle="MongoDB Migration"
	description="MongoDB Migration"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636784,32738475"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-mongodbmigration"
	displayOrder="224"
	category="MongoDB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Import MongoDB data into CosmosDB

## **Recommended Steps**

### **Migrating Mongo DB Data to Cosmos DB**  
To migrate data from MongoDB to an Azure Cosmos DB account for use with the API for MongoDB, you must:

* Download either mongoimport.exe or mongorestore.exe from the [MongoDB Download Center](https://www.mongodb.com/download-center).
* Get your [API for MongoDB connection string](https://docs.microsoft.com/azure/cosmos-db/connect-mongodb-account).
* Throughput that you provision directly impacts the directly impacts the duration of migration. Consider increasing RUs during migration and scaling down once they complete.

### **Updating Mongo DB 3.2 to 3.6**  
All new accounts provisioned using Azure Portal will have the option to provision with server version 3.6.  
For existing accounts a support ticket to update is required and the update will change the server version. While generally 3.6 is compatible with 3.2, it is recommended a customer provision a new account through the portal and select the Mongo DB server version 3.6 to try it out with their application on a dev or qa instance before considering updating the account backing any production workload.  

### **Using 3.2 and 3.6**
Upgrading to 3.6 does not mean you have to stop using 3.2 style change feed. All features of 3.2 continue to be supported in 3.6, even the 3.2 endpoint will remain operational for certain client applications you wish to keep on 3.2 for longer than others. The 3.6 update does not move or alter the data as it is at the API and not the storage layer.  




## **Recommended Documents**

[Azure Cosmos DB Mongo DB 3.6 Feature Support](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
<br>Azure Cosmos DB API for MongoDB (3.6 version) supported features and syntax


Refer the [MongoDB Migrate Page](https://docs.microsoft.com/azure/cosmos-db/mongodb-migrate) for ways to import data for MongoDB using tools like mongoimport, mongorestore. Additionally, the document provides some [guidelines for successful migration](https://docs.microsoft.com/azure/cosmos-db/mongodb-migrate#guide-for-a-successful-migration)
