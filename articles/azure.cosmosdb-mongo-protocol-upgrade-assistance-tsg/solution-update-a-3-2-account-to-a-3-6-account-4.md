<properties
	  pageTitle="Update a 3.2 account to a 3.6 account"
	  description="Update a 3.2 account to a 3.6 account"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="dd4dda22-6730-4633-a0cb-04ddbd225025"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Update a 3.2 account to a 3.6 account

<!--issueDescription-->

Dear customer,

I would like to mention that your account is using version 3.2, and now we do have an updated version of 3.6. Updating to 3.6 would help in this scenario. 

Upgrading to the latest version of the service will provide the most up to date functionality, as well as enhancements in performance, stability, and the latest fixes.

The upgrade process will not provide any service interruptions or downtime. It will also not require any data or index migrations. As soon as you start the process, your account will be queued to proceed with the upgrade. You will be notified when your account has finished upgrading.

Benefits of upgrading to version 3.6:
. Enhanced performance and stability
. Support for new database commands
. Support for aggregation pipeline by default and new aggregation stages
. Support for ChangeStream
. Support for Compound Indexes
. Cross-partition support for the following operations: UPDATE, DELETE, COUNT, and ORDER BY
. Improved performance for the following aggregate operations: COUNT, SKIP, LIMIT, and GROUP BY
. Changes from previous engine versions

MongoDB collections will only have the _id property indexed by default

Action Required:
The connection string to the MongoDB service in your application will need to be updated as shown in the Overview dashboard of the Azure Portal. The updated endpoint is: ACCOUNTNAME.mongo.cosmos.azure.com but it might differ if your account is in a Sovereign, Government, or Restricted Azure cloud.

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
- Option is visible: If the option is enabled for you, clicking the *Enable* button will start the migration. It will show as *Pending* in the features list for up to a couple of days. When it has completed, the account will show new connection strings in the Portal with `*.mongo.cosmos.azure.com`   

**Important Note:** While generally 3.6 is compatible with 3.2, it is recommended a customer provision a new account through the portal and select the MongoDB server version 3.6 to try it out with their application on a dev or qa instance before considering updating the account backing any production workload. 


### **Connecting to 3.6 after migration**
Note that when using Azure Cosmos DB's API for MongoDB accounts, the 3.6 version of accounts have the endpoint in the format `*.mongo.cosmos.azure.com` whereas the 3.2 version of accounts have the endpoint in the format `*.documents.azure.com`.

### **Using 3.2 and 3.6**
Upgrading to 3.6 does not mean you have to stop using 3.2 style change feed. All features of 3.2 continue to be supported in 3.6, even the 3.2 endpoint will remain operational for certain client applications you wish to keep on 3.2 for longer than others. The 3.6 update does not move or alter the data as it is at the API and not the storage layer.  




## **Recommended Documents:**
https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-version-upgrade

https://devblogs.microsoft.com/cosmosdb/upgrade-your-server-version-from-3-2-to-3-6-for-azure-cosmos-db-api-for-mongodb/

[Azure Cosmos DB MongoDB 3.6 Feature Support](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
<br>Azure Cosmos DB API for MongoDB *3.6 version* supported features and syntax

[MongoDB pre-Migration Guide](https://docs.microsoft.com/azure/cosmos-db/mongodb-pre-migration)
<br>Before you migrate your data from MongoDB (either on-premises or in the cloud) to Azure Cosmos DB's API for MongoDB, this guide provides steps you should do.

[MongoDB Migrate Page](https://docs.microsoft.com/azure/cosmos-db/mongodb-migrate)
<br>Ways to import data for MongoDB using tools like mongoimport, mongorestore.   

[MongoDB post-Migration Guide](https://docs.microsoft.com/azure/cosmos-db/mongodb-post-migration)
<br>After you migrate the data stored in MongoDB database to Azure Cosmos DB's API for MongoDB, you can connect to Azure Cosmos DB and manage the data. This guide provides the steps you should consider after the migration.

https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-feature-support
https://docs.microsoft.com/en-us/azure/cosmos-db/connect-mongodb-account

Thank you.

<!--/issueDescription-->

