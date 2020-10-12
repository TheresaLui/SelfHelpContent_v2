<properties
	pageTitle="Change feed in Azure Cosmos DB"
	description="Troubleshoot Azure Cosmos DB Change feed issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="ealsur"
	ms.author="maquaran"
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

### **Change feed processor versions**

* The V2 .NET change feed processor is available on [Nuget](https://www.nuget.org/packages/Microsoft.Azure.DocumentDB.ChangeFeedProcessor/) and the source code on [GitHub](https://github.com/Azure/azure-documentdb-changefeedprocessor-dotnet/)
* The newer V3 .NET change feed processor is part of the .NET V3 SDK and included in the [SDK Nuget](https://www.nuget.org/packages/Microsoft.Azure.Cosmos) and the source code is also on [GitHub](https://github.com/Azure/azure-cosmos-dotnet-v3)

Make sure you have updated to the latest version, as the issue you might be encountering may have already been solved.

### **Why is a lease container required for the change feed processor?**

There are four main components of implementing the change feed processor:

1. **The monitored container:** The monitored container has the data from which the change feed is generated. Any inserts and updates to the monitored container are reflected in the change feed of the container.

1. **The lease container:** The lease container acts as a state storage and coordinates processing the change feed across multiple workers. The lease container can be stored in the same account as the monitored container or in a separate account.

1. **The host:** A host is an application instance that uses the change feed processor to listen for changes. Multiple instances with the same lease configuration can run in parallel, but each instance should have a different **instance name**.

1. **The delegate:** The delegate is the code that defines what you, the developer, want to do with each batch of changes that the change feed processor reads. 

The lease container is particularly used to store the last processed point of the Change Feed in case the host stops. If the host starts again at a later point in time, the Processor will continue from the latest point in time stored in the lease container. The lease container is also used to do dynamic load balancing when multiple instances of the Processor are running.

### **Error handling and exceptions in the change feed processor**

If your current Delegate or Observer (if you are working with V2 .NET) throws an *unhandled exception*, the processor will stop the current thread handling that batch of changes and eventually retry it. The retry will keep happening until your code no longer throws an unhandled exception processing that batch of changes. Always make sure you are handling correctly all expected error conditions.

### **How do I scale and use multiple instances?**

The change feed processor can distribute compute across multiple instances automatically. You can deploy multiple instances of your application using the change feed processor and take advantage of it, the only key requirements are:

1. All instances should have the same lease container configuration
1. All instances should have the same workflow or processor name. In the case of V2, this is the `LeaseCollectionPrefix` configuration.
1. Each instance needs to have a different instance name (`WithInstanceName`).

### **Some of my change feed processor instances are idle and not processing changes**

The change feed processor creates one lease document in the lease container per physical partition on the monitored container. The change feed processor distributes lease documents across existing instances using an equal distribution algorithm (for example, if you have 10 lease documents and 5 instances, it will assign 2 lease documents per host). When new instances are added or removed, a rebalancing takes place. 

If the amount of instances is greater than the amount of lease documents (greater than the amount of physical partitions) those extra instances will remain idle. This means that the current implementation's degree of parallelism is limited by the number of physical partitions.

### **The changes are not detected quickly enough**

The normal life cycle of a host instance is:

1. Read the change feed
1. If there are no changes, sleep for a predefined amount of time (customizable with `WithPollInterval` in the Builder) and go to #1
1. If there are changes, send them to the **delegate**
1. When the delegate finishes processing the changes **successfully**, update the lease store with the latest processed point in time and go to #1

To make sure that latency is optimized:

1. Make sure your change feed processor is co-located with a Cosmos DB account region, and you are using `CosmosClientOptions.ApplicationRegion` / `CosmosClientOptions.PreferredRegions` (V3 .NET) or `ConnectionPolicy.PreferredLocations` (V2 .NET) to indicate which region you are running on.
1. Are the changes happening in your Azure Cosmos container continuous or sporadic?
    * If they are sporadic, there could be some delay between the changes being stored and the Azure Function picking them up. Based on the life cycle explained previously, you can customize the sleeping period through the Poll interval.
	* If they are continuous, the speed at which new changes are read from the change feed are also defined by the speed at which you can process them. The faster you can process them, the faster new changes can be read.

## **Recommended Documents**

[Change feed in Azure Cosmos DB - overview](https://docs.microsoft.com/azure/cosmos-db/change-feed)
<br>Change feed support in Azure Cosmos DB works by listening to an Azure Cosmos container for any changes. It then outputs the sorted list of documents that were changed in the order in which they were modified. The changes are persisted, can be processed asynchronously and incrementally, and the output can be distributed across one or more consumers for parallel processing.  

[Reading Azure Cosmos DB change feed](https://docs.microsoft.com/azure/cosmos-db/read-change-feed)
<br>This article describes how you can work with the Azure Cosmos DB change feed using any of the following options:
* Using Azure Functions
* Using the change feed processor library
* Using the Azure Cosmos DB SQL API SDK  

[Change feed processor in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/change-feed-processor)
<br>This article covers the overview details of change feed processor V3.

[Migrate from Change feed processor V2 to V3](https://docs.microsoft.com/azure/cosmos-db/how-to-migrate-from-change-feed-library)
<br>This article covers the migration steps to go from V2 to V3.

[Diagnose and troubleshoot issues when using Azure Cosmos DB Trigger in Azure Functions](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-changefeed-functions)
<br>This article covers common issues, workarounds, and diagnostic steps, when you use the Azure Functions trigger for Cosmos DB.  

[How to configure and read the Azure Cosmos DB Trigger logs](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-cosmos-db-trigger-logs)
<br>This article describes how you can configure your Azure Functions environment to send the Azure Functions trigger for Cosmos DB logs to your configured monitoring solution.  



