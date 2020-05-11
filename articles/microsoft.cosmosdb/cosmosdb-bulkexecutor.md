<properties
	pageTitle="Azure Cosmos DB bulk executor library"
	description="Troubleshoot Azure Cosmos DB bulk executor library"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636772"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-bulkexecutor"
	displayOrder="120"
	category="Tools and Connectors"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB bulk executor library
Most users are able to resolve their Cosmos DB bulk executor issue using the steps below.

## **Recommended Steps**

Azure Cosmos DB is a fast, flexible, and globally distributed database service that is designed to elastically scale out to support:

* Large read and write throughput (millions of operations per second).
* Storing high volumes of (hundreds of terabytes, or even more) transactional and operational data with predictable millisecond latency.

The bulk executor library helps you leverage this massive throughput and storage. The bulk executor library allows you to perform bulk operations in Azure Cosmos DB through bulk import and bulk update APIs. You can read more about the features of bulk executor library in the following sections.

### **.NET - High CPU usage**
Bulk executor normally uses higher CPU due to the internal processes that group and process the input documents. There are known scenarios where unexpected high CPU can occur:

1. Older versions of the Bulk Executor library: Version 1.8.2 [included fixes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-bulk-executor-dot-net#182) to CPU utilization, make sure you are using the latest release (`1.X` for NET Framework applications, `2.X` for NET Core applications) and update if not.
1. Concurrent usage: Bulk Executor import and update APIs are **not thread-safe**. There should not be concurrent calls to the import and update APIs from multiple threads. If this is the case, you need to convert those concurrent calls to sequential calls or potentially use a single call with the sum of all documents.

### **.NET - Deadlocks**
Locks are often caused by logging or tracing listeners with disk or other resource contention locks. 

1. Verify you are using the latest release (`1.X` for NET Framework applications, `2.X` for NET Core applications) and update if not. There were [improvements](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-bulk-executor-dot-net#182) in the latest versions that use TraceSource instead of the DefaultTrace.
1. Verify that your application configuration is not using the system default trace listener. By default, NET Framework applications will use the system default trace listener that is disk bound. Make sure you [remove the default trace listener](https://docs.microsoft.com/dotnet/framework/configure-apps/file-schema/trace-debug/remove-element-for-listeners-for-trace#example) and manually add one just for the `BulkExecutorTrace` source.
1. Verify your trace listeners are saving in a medium that is not generating any locks. Obtaining a process dump during the deadlock will point to the deadlock source, if it's related to `System.Diagnostics` or a class related to your trace listeners, the deadlock source is there. Try removing all listeners and verifying if the problem is solved.
1. Avoid blocking calls. Bulk Executor API calls are async, use the `await/async` pattern and avoid `Wait()`, `.Result`, or `.GetAwaiter().GetResult()` calls that can lead to thread locking in some environments.

## **Recommended Documents**
[Azure Cosmos DB bulk executor library overview](https://docs.microsoft.com/azure/cosmos-db/bulk-executor-overview)
<br>The bulk executor library helps you leverage this massive throughput and storage. The bulk executor library allows you to perform bulk operations in Azure Cosmos DB through bulk import and bulk update APIs.   

[Use bulk executor .NET library to perform bulk operations in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/bulk-executor-dot-net)
<br>This tutorial provides instructions on using the bulk executor .NET library to import and update documents to an Azure Cosmos container.   

[Bulk executor .NET library performance tips](https://docs.microsoft.com/azure/cosmos-db/bulk-executor-dot-net#performance-tips)
<br>Review the performance best practices while using the Bulk Executor library.

[New .NET V3 SDK Bulk support](https://docs.microsoft.com/azure/cosmos-db/how-to-migrate-from-bulk-executor-library)
<br>For new applications, the recommendation is to use the new Azure Cosmos DB V3 SDK, which already has support for Bulk. This article is a migration guide.

[Use bulk executor Java library to perform bulk operations on Azure Cosmos DB data](https://docs.microsoft.com/azure/cosmos-db/bulk-executor-java)
<br>This tutorial provides instructions on using the Azure Cosmos DBs bulk executor Java library to import, and update Azure Cosmos DB documents. 
