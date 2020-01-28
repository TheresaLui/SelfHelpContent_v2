<properties
	pageTitle="MongoDB Migration"
	description="MongoDB Migration"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636784"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-mongodbmigration"
	displayOrder="224"
	category="MongoDB"
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
For existing accounts a support ticket to update is required and the update will change the server version. While generally 3.6 is compatible with 3.2, it is recommended a customer provision a new account through the portal and select the Mongo DB server version 3.6 try it out with their application on a dev or qa instance before considering updating the account backing any production workload.  


### **Cosmos DB Mongo DB 3.6 New Features**  
Please see [Mongo DB 3.6 Supported Features and Syntax] (https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-feature-support-36)
* Support for new commands/aggregation stages added in v3
* Support for ChangeStream  (ChangeFeed via changestream)
* Support for Compound indexes
* Support for unsharded collections in databases with throughput
* Support for cross-partition UPDATE/DELETE/COUNT
* Support for cross-partition ORDERBY
* Support for aggregate pushdown for Count
* Support for SKIP/LIMIT pushdown
* Support for GROUPBY pushdown for supported queries
* The 40 MB limit is only removed on server version 3.6. It is recommended the customer create a new account on server version 3.6, or request we update this existing account to server version 3.6. 
 
**Changes from v3.2**  
* Mongo collections will only have *_id* index by default vs auto-indexing (as with Mongo v3.2 stack)
* Mongo service will not retry on 429s (Mongo v3.2 stack did 10 retries before returning RateLimiting error to client)
* Per request timeout is increased from 15 seconds to 30 seconds
* Idle connection timeout is increased from 30 minutes to 5 hours 




## **Recommended Documents**

[Azure Cosmos DB Mongo DB 3.6 Feature Support](https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-feature-support-36)
<br>Azure Cosmos DB API for MongoDB (3.6 version) supported features and syntax


Refer the [MongoDB Migrate Page](https://docs.microsoft.com/azure/cosmos-db/mongodb-migrate) for ways to import data for MongoDB using tools like mongoimport, mongorestore. Additionally, the document provides some [guidelines for successful migration](https://docs.microsoft.com/azure/cosmos-db/mongodb-migrate#guide-for-a-successful-migration)
