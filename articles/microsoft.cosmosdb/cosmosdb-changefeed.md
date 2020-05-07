<properties
	pageTitle="Change feed in Azure Cosmos DB"
	description="Troubleshoot Azure Cosmos DB Change feed issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636774,32636775,32684532"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-changefeed"
	displayOrder="61"
	category="Core (SQL)"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Change feed in Azure Cosmos DB

Change feed support in Azure Cosmos DB works by listening to an Azure Cosmos DB container for any changes. It then outputs the sorted list of documents that were changed in the order in which they were modified. The changes are persisted, can be processed asynchronously and incrementally, and the output can be distributed across one or more consumers for parallel processing.

## **Recommended Steps**

### **Stored procedure cannot insert due to partition key mismatch**
*CancellationToken* parameter in *ExecuteStoredProcedureAsync* should be given as the 3rd parameter. If it is not in the expected order, the payload will be incorrect.  



## **Recommended Documents**

[Diagnose and troubleshoot issues when using Azure Cosmos DB Trigger in Azure Functions](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-changefeed-functions)
<br>This article covers common issues, workarounds, and diagnostic steps, when you use the Azure Functions trigger for Cosmos DB.  

[Change feed in Azure Cosmos DB - overview](https://docs.microsoft.com/azure/cosmos-db/change-feed)
<br>Change feed support in Azure Cosmos DB works by listening to an Azure Cosmos container for any changes. It then outputs the sorted list of documents that were changed in the order in which they were modified. The changes are persisted, can be processed asynchronously and incrementally, and the output can be distributed across one or more consumers for parallel processing.  

[Reading Azure Cosmos DB change feed](https://docs.microsoft.com/azure/cosmos-db/read-change-feed)
<br>This article describes how you can work with the Azure Cosmos DB change feed using any of the following options:
* Using Azure Functions
* Using the change feed processor library
* Using the Azure Cosmos DB SQL API SDK  

[Change feed processor in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/change-feed-processor)
<br>This article covers the four main components of implementing the change feed processor:
* The monitored container
* The lease container
* The host
* The delegate  

[How to configure and read the Azure Cosmos DB Trigger logs](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-cosmos-db-trigger-logs)
<br>This article describes how you can configure your Azure Functions environment to send the Azure Functions trigger for Cosmos DB logs to your configured monitoring solution.  



