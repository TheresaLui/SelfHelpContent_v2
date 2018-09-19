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

Cosmos DB has a timeout limit for all operation and has to complete within in the timeout duration.  The application is returned with timeout if the given operation did not complete within the timeout period.  All Server Side execution has to check for the return value "isAccepted" and handle based on the returned value.  

The best practice for any bulk operation using Server Side programming is to implement batching using top 100 or 1000. The Server Side call  should be returned as soon the batch limit are reached. The client application can then call the Server Side code again in a loop to complete the bulk process.

Please proceed to create the Support Ticket if you are getting timeout other than the above scenario


## **Recommended documents**

* [Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://github.com/balaksms/SelfHelpContent/edit/master/articles/microsoft.documentdb/documentdb-admin-requesttimeout.md)

* [Bounded execution](https://docs.microsoft.com/en-us/azure/cosmos-db/programming#bounded-execution)

* [Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)

* [Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)

* [Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java)
