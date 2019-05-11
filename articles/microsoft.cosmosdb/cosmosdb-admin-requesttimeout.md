<properties
	pageTitle="Request Timeout"
	description="Request Timeout"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	ms.author="balaks"
	selfHelpType="generic"
	supportTopicIds="32636823"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-admin-requesttimeout"
/>

# Server-side stored procedure, trigger, or UDF returns timeouts

The application should check for the return value of the operation and handle any timeouts appropriately.  All server-side execution must check for the return value "isAccepted" and handle based on the return value.  

The best practice for any bulk operation using server-side programming is to implement batching using top 100 or 1000. The server-side call  should be returned as soon as the batch limit is reached. The client application can then call the server-side code again in a loop to complete the bulk process.

Please proceed to create a support ticket if you are getting timeouts for non bulk operations.


## **Recommended documents**

* [Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs)
* [Bounded execution](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs#bounded-execution)
* [Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
* [Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)
* [Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java)
