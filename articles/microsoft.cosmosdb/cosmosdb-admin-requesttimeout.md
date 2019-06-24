<properties
	pageTitle="Request Timeout"
	description="Request Timeout"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="markjbrown"
	ms.author="mjbrown"
	selfHelpType="generic"
	supportTopicIds="32636823"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-admin-requesttimeout"
/>

# Timeouts in Cosmos DB

Stored procedure requests have a timeout of [5 seconds](https://docs.microsoft.com/azure/cosmos-db/concepts-limits). Stored procedures must yield execution by checking the `isAccepted` return value in order to avoid running into timeouts (408). See [Stored procedure sample using IsAccepted](https://github.com/Azure/azure-cosmos-dotnet-v2/blob/fd036405a7de6b8bc4c9fdbc6872b09f9b6e2bf3/samples/code-samples/ServerSideScripts/JS/BulkImport.js#L50-L58) for a sample that breaks up and resumes execution using this pattern.

## **Recommended Steps**

* For stored procedures, follow the pattern above to avoid timeouts
* For any other operation (not stored procedures) that return a timeout response, please file a support ticket with the account endpoint, database and container names, activity ID, and the operation that timed out

## **Recommended Documents**

* [Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs)
* [Bounded execution](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs#bounded-execution)
