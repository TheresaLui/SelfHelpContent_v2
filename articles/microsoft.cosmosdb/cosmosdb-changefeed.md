<properties
	pageTitle="Change feed in Azure Cosmos DB"
	description="Troubleshoot Azure Cosmos DB Change feed issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="rnagpal"
	ms.author="rnagpal"
	selfHelpType="generic"
	supportTopicIds="32636774,32636775,32684532"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-changefeed"
	displayOrder="61"
	category="Core (SQL)"
/>

# Change feed in Azure Cosmos DB

Change feed support in Azure Cosmos DB works by listening to an Azure Cosmos DB container for any changes. It then outputs the sorted list of documents that were changed in the order in which they were modified. The changes are persisted, can be processed asynchronously and incrementally, and the output can be distributed across one or more consumers for parallel processing.

## **Recommended Steps**

To learn more about Change Feed, see the following recommended documents.

## **Recommended Documents**

* [Change feed in Azure Cosmos DB - overview](https://docs.microsoft.com/azure/cosmos-db/change-feed)
* [Reading Azure Cosmos DB change feed](https://docs.microsoft.com/azure/cosmos-db/read-change-feed)
* [Change feed processor in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/change-feed-processor)
* [How to configure and read the Azure Cosmos DB Trigger logs](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-cosmos-db-trigger-logs)
* [Diagnose and troubleshoot issues when using Azure Cosmos DB Trigger in Azure Functions](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-changefeed-functions)


