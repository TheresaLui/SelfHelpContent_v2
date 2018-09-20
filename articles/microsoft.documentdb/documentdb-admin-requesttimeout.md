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

# Stored Procedure execution returns timeouts

Cosmos DB has a timeout limit for all operations and has to complete within the timeout duration.  The application returns timeout error if the given operation did not complete within the timeout period.  All server side execution have to check for the return value "isAccepted" and handle based on the returned value.  

The best practice for any bulk operation using server side programming is to implement batching using top 100 or 1000. The Server Side call  should be returned as soon the batch limit are reached. The client application can then call the server side code again in a loop to complete the bulk process.

Please proceed to create the Support Ticket if you are getting timeout other than the above scenario.


## **Recommended documents**

* [Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://docs.microsoft.com/azure/cosmos-db/programming)
* [Bounded execution](https://docs.microsoft.com/azure/cosmos-db/programming#bounded-execution)
* [Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
* [Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)
* [Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java)
