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

# Import MongoDB data into Cosmos DB

## **Recommended Steps**

### **Migrating MongoDB Data to Cosmos DB**  
To migrate data from MongoDB to an Azure Cosmos DB account for use with the API for MongoDB, you must:

* Download either mongoimport.exe or mongorestore.exe from the [MongoDB Download Center](https://www.mongodb.com/download-center).
* Get your [API for MongoDB connection string](https://docs.microsoft.com/azure/cosmos-db/connect-mongodb-account).
* Throughput that you provision directly impacts the directly impacts the duration of migration. Consider increasing RUs during migration and scaling down once they complete.  


### **Updating MongoDB 3.2 to 3.6**  
The Azure Cosmos DB's API for MongoDB is compatible with MongoDB server version **3.6** by default for new accounts.   

For existing accounts, navigate to the Settings -> Features area of your Cosmos DB Mongo account. The option titled *Upgrade to Mongo server version 3.6* should be visible. 
- Option not visible: If this option does not appear for your account, you must file a support ticket request.  
- Option is visible: If the option is enabled for you, clicking the *Enable* button will start the migration. It will show as *Pending* in the features list for up to a couple of days. When it has completed, the account will show new connection strings in the Portal with `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.mongo.cosmos.azure.com` but it might differ if your account is in a Sovereign, Government, or Restricted Azure cloud.  

**Important Note:** While generally 3.6 is compatible with 3.2, it is recommended a customer provision a new account through the portal and select the MongoDB server version 3.6 to try it out with their application on a dev or qa instance before considering updating the account backing any production workload. 


### **Connecting to 3.6 after migration**
Note that when using Azure Cosmos DB's API for MongoDB accounts, the 3.6 version of accounts have the endpoint in the format `<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->.mongo.cosmos.azure.com` whereas the 3.2 version of accounts have the endpoint in the format `*.documents.azure.com`.


### **Using 3.2 and 3.6**
Upgrading to 3.6 does not mean you have to stop using 3.2 style change feed. All features of 3.2 continue to be supported in 3.6, even the 3.2 endpoint will remain operational for certain client applications you wish to keep on 3.2 for longer than others. The 3.6 update does not move or alter the data as it is at the API and not the storage layer.  




## **Recommended Documents**

[Azure Cosmos DB MongoDB 3.6 Feature Support](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
<br>Azure Cosmos DB API for MongoDB *3.6 version* supported features and syntax

[MongoDB pre-Migration Guide](https://docs.microsoft.com/azure/cosmos-db/mongodb-pre-migration)
<br>Before you migrate your data from MongoDB (either on-premises or in the cloud) to Azure Cosmos DB's API for MongoDB, this guide provides steps you should do.

[MongoDB Migrate Page](https://docs.microsoft.com/azure/cosmos-db/mongodb-migrate)
<br>Ways to import data for MongoDB using tools like mongoimport, mongorestore.   

[MongoDB post-Migration Guide](https://docs.microsoft.com/azure/cosmos-db/mongodb-post-migration)
<br>After you migrate the data stored in MongoDB database to Azure Cosmos DB's API for MongoDB, you can connect to Azure Cosmos DB and manage the data. This guide provides the steps you should consider after the migration.
