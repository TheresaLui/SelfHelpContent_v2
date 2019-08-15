<properties
	pageTitle="Azure Cosmos DB Triggers"
	description="Configure Azure Cosmos DB Triggers"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="rnagpal"
	ms.author="rnagpal"
	selfHelpType="resource"
	supportTopicIds="32636793"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-function-triggers"
	displayOrder="123"
	category="Tools and Connectors"
/>

# Azure Functions trigger for Cosmos DB

## Prerequisites

Always make sure you are running the latest version of the [Azure Cosmos DB Extension package for Functions](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-changefeed-functions#dependencies).

## Function not receiving any or partial set of changes

### Availability

The Azure Functions trigger for Cosmos DB currently reads the Change Feed through the **Core (SQL) API**, that means that Mongo, Cassandra, and Table accounts are not yet supported.

### Connectivity

Verify that your Azure Cosmos account's [Firewall configuration](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall) has Azure datacenters enabled or the Virtual Network your Function App is associated with (in case you are working with [App Service or Premium Plan](https://docs.microsoft.com/azure/azure-functions/functions-scale#hosting-plan-support)), whitelisted.

### Error handling

The Azure Functions trigger for Cosmos DB, by default, **won't retry** a batch of changes if there was an **unhandled exception** during your code execution. This means that, if not handled correctly, when a batch of changes is received by your Function, execution can be stopping and inherently losing part of the batch.

Make sure your Function's code has `try/catch` blocks, especially within any loop, to make sure that any failure in processing one document, does not exit the loop.

### Multiplicity

The most common scenario, once connectivity and availability problems have been ruled out, is having multiple Azure Functions listening to the **same Monitored Collection** and using the **same Lease Collection**. When two or more Triggers share the same monitored and lease collection, the locking and load balancing algorithm will probably let one of them own the leases, while leaving the other Function out. This is expected, as these configurations should not be duplicated in multiple Triggers.

* If you want multiple Triggers to work independently, listening for changes in the same Monitored Collection, and also share the same Lease Collection for cost optimizations, you need to [configure them with different Prefixes](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-cosmos-db-trigger-logs).
* If you are unsure or don't know about extra Azure Functions running but you know how many Azure Function App instances you have running, you can inspect your Lease Collection and count the number of lease documents within, the distinct values of the `Owner` property in them should be equal to the number of instances of your Function App. If there are more Owners than the known Azure Function App instances, it means that these extra owners are the one "stealing" the changes. In that case, you can mitigate the situation by [configuring a different Prefix](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-cosmos-db-trigger-logs).

## Delay in receiving changes

The rate at which the changes are delivered to your Function depends greatly on the speed at which your Function processes each batch. If the rate at which the changes are happening in the Monitored Collection is greater than the rate at which your Function processes them, there will be an increasing lag.

1. Is your Azure Function deployed in the same region as your Azure Cosmos account? For optimal network latency, both the Azure Function and your Azure Cosmos account should be colocated in the same Azure region.
2. Are the changes happening in your Azure Cosmos container continuous or sporadic? If it's the latter, there could be some delay between the changes being stored and the Azure Function picking them up. This is because internally, when the trigger checks for changes in your Azure Cosmos container and finds none pending to be read, it will sleep for a configurable amount of time (5 seconds, by default) before checking for new changes (to avoid high RU consumption). You can configure this sleep time through the `FeedPollDelay/feedPollDelay` setting in the [configuration](https://docs.microsoft.com/azure/azure-functions/functions-bindings-cosmosdb-v2#trigger---configuration) of your trigger (the value is expected to be in milliseconds).
3. Your Azure Cosmos container might be [rate-limited](https://docs.microsoft.com/azure/cosmos-db/request-units)
4. You can use the `PreferredLocations` attribute in your trigger to specify a comma-separated list of Azure regions to define a custom preferred connection order
5. If working on App Service/Premium Plan, you can increase the number of instances or the size of the instances to accommodate your compute/processing needs
6. Try and optimize the Function to do as few things as possible to reduce execution time, you can always apply a Fan-Out pattern for any lengthy operation

## **Recommended Documents**

* [Introduction](https://docs.microsoft.com/azure/cosmos-db/change-feed)
* [How to configure and read the Azure Cosmos DB Trigger logs](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-cosmos-db-trigger-logs)
* [Create multiple Azure Cosmos DB Triggers](https://docs.microsoft.com/azure/cosmos-db/how-to-create-multiple-cosmos-db-triggers)
* [Diagnose and troubleshoot issues when using Azure Cosmos DB Trigger in Azure Functions](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-changefeed-functions)
