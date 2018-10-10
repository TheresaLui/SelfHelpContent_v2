<properties
	pageTitle="MongoDB Migration"
	description="MongoDB Migration"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds="32597508"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Import MongoDB data into CosmosDB

To migrate data from MongoDB to an Azure Cosmos DB account for use with the API for MongoDB, you must:

* Download either mongoimport.exe or mongorestore.exe from the [MongoDB Download Center](https://www.mongodb.com/download-center).
* Get your [API for MongoDB connection string](https://docs.microsoft.com/azure/cosmos-db/connect-mongodb-account).
* Make sure you pre-create and scale up your collections 

After that, use the [Data Migration Tool](https://docs.microsoft.com/azure/cosmos-db/import-data) to import data into CosmosDB

## **Recommended documents**
Refer the [MongoDB Migrate Page](https://docs.microsoft.com/azure/cosmos-db/mongodb-migrate) for ways to import data for MongoDB using tools like mongoimport, mongorestore. Additionally, the document provides some [guidelines for successful migration](https://docs.microsoft.com/azure/cosmos-db/mongodb-migrate#guide-for-a-successful-migration)
