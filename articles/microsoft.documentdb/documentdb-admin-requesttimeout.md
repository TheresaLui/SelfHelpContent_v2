<properties
	pageTitle="Request Timeout"
	description="Request Timeout"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="85"
	selfHelpType="resource"
	supportTopicIds="32597555"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Server-side (stored procedure/triggers/UDFs) returns timeouts

The application should check for the return value and handle the timeout.  All server-side execution must check for the return value "isAccepted" and handle based on the return value.  

The best practice for any bulk operation using server-side programming is to implement batching using top 100 or 1000. The server-side call  should be returned as soon the batch limit are reached. The client application can then call the server-side code again in a loop to complete the bulk process.

Please proceed to create the support ticket if you are getting timeout other than the above scenario.


## **Recommended documents**

* [Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://docs.microsoft.com/azure/cosmos-db/programming)
* [Bounded execution](https://docs.microsoft.com/azure/cosmos-db/programming#bounded-execution)
* [Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
* [Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)
* [Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java)
