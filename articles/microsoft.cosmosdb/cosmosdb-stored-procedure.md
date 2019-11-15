<properties
	pageTitle="Stored procedure programming"
	description="Stored Procedure programming"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="resource"
	supportTopicIds="32636829"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-stored-procedure"
	displayOrder="66"
	category="Core (SQL)"
/>

# Troubleshooting stored procedures

## **Recommended Steps**

### Stored Procedures
* Stored procedure requests have a timeout of [5 seconds](https://docs.microsoft.com/azure/cosmos-db/concepts-limits). Stored procedures must yield execution by checking the `isAccepted` return value in order to avoid running into timeouts (408). See [Stored procedure sample using IsAccepted](https://github.com/Azure/azure-cosmos-dotnet-v2/blob/fd036405a7de6b8bc4c9fdbc6872b09f9b6e2bf3/samples/code-samples/ServerSideScripts/JS/BulkImport.js#L50-L58) for a sample that breaks up and resumes execution using this pattern
* You can debug stored procedures locally using the [Cosmos DB Emulator](https://docs.microsoft.com/azure/cosmos-db/local-emulator) or by adding console.log statements and enabling [Enable Script Logging RequestOption in .NET](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.requestoptions.enablescriptlogging?view=azure-dotnet) or [Enable Script Logging RequestOption in Java](https://docs.microsoft.com/java/api/com.microsoft.azure.documentdb.requestoptions.setscriptloggingenabled?view=azure-java-stable#com_microsoft_azure_documentdb_RequestOptions_setScriptLoggingEnabled_boolean_) via RequestOptions
* Stored procedures return 400 (Bad Request) on any failure. You can examine the inner exception by examining the `x-ms-substatus` response header
* Stored procedures are recommended for write operations. You may run into RU bottlenecks if you use stored procedures for readonly operations
* Stored procedures are scoped to a single partition key specified via [Partition Key RequestOption in .NET](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.requestoptions.partitionkey?view=azure-dotnet) or [Partition Key RequestOption in Java](https://docs.microsoft.com/java/api/com.microsoft.azure.documentdb.requestoptions.setpartitionkey?view=azure-java-stable#com_microsoft_azure_documentdb_RequestOptions_setPartitionKey_PartitionKey_). Queries within a stored procedure are also automatically scoped to the same partition key value



## **Recommended Documents**

* [Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs)  
Azure Cosmos DB provides language-integrated, transactional execution of JavaScript. When using the SQL API in Azure Cosmos DB, you can write stored procedures, triggers, and user-defined functions (UDFs) in the JavaScript language. You can write your logic in JavaScript that executed inside the database engine. You can create and execute triggers, stored procedures, and UDFs by using Azure portal, the JavaScript language integrated query API in Azure Cosmos DB or the Cosmos DB SQL API client SDKs.
<br>

* [How to register and use stored procedures, triggers, and user-defined functions in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs)  
The SQL API in Azure Cosmos DB supports registering and invoking stored procedures, triggers, and user-defined functions (UDFs) written in JavaScript. You can use the SQL API .NET, .NET Core, Java, JavaScript, Node.js, or Python SDKs to register and invoke the stored procedures. Once you have defined one or more stored procedures, triggers, and user-defined functions, you can load and view them in the Azure portal by using Data Explorer.


* [Cosmos DB Server-side JavaScript API](https://azure.github.io/azure-cosmosdb-js-server/)