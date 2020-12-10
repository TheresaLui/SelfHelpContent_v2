<properties
	pageTitle="MongoDB How-to"
	description="MongoDB How-to"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32783701"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-mongodb-howto"
	displayOrder="231"
	category="MongoDB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# MongoDB - How-to

Most users are able to resolve their Cosmos DB related MongoDB How-to questions or issues using the steps below.  

### **Migrating MongoDB Data to Cosmos DB**  

To migrate data from MongoDB to an Azure Cosmos DB account for use with the API for MongoDB, you must:

* Download either `mongoimport.exe` or `mongorestore.exe` from the [MongoDB Download Center](https://www.mongodb.com/download-center).
* Get your [API for MongoDB connection string](https://docs.microsoft.com/azure/cosmos-db/connect-mongodb-account).

**Note:** Throughput that you provision directly impacts the duration of migration. Consider increasing RUs during migration and scaling down after they complete. 



## **Recommended Documents**

[Azure Cosmos DB's API for MongoDB (3.6 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
<br>The Azure Cosmos DB's API for MongoDB is compatible with MongoDB server version 3.6 by default for new accounts. The supported operators and any limitations or exceptions are listed in this article. Any client driver that understands these protocols should be able to connect to Azure Cosmos DB's API for MongoDB.  

[Azure Cosmos DB's API for MongoDB (3.2 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support)
<br>This article covers MongoDB version 3.2. The supported operators and any limitations or exceptions are listed in this article.  

[Performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>This article describes how you can improve your database performance.  

[Aggregation pipeline support](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support#aggregation-pipeline)




