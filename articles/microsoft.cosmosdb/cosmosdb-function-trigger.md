<properties
	pageTitle="Azure Functions and database triggers"
	description="Issues with Azure Cosmos DB in Azure Functions and database triggers"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="ealsur"
	ms.author="maquaran"
	selfHelpType="generic"
	supportTopicIds="32636793,32688843"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-function-triggers"
	displayOrder="123"
	category="Tools and Connectors"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Functions with Cosmos DB and database triggers
This article covers the most common issues with Azure Cosmos DB database triggers and using Azure Functions.

## **Recommended Steps**

### **Database Triggers**
*Note:*  Registered triggers do not run automatically when their corresponding operations (create / delete / replace / update) happen. They have to be explicitly called when executing these operations.  

Azure Cosmos DB supports two types of triggers:
* [Pre-triggers](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#pre-triggers)
<br>Azure Cosmos DB provides triggers that can be invoked by performing an operation on an Azure Cosmos item. For example, you can specify a pre-trigger when you are creating an item. In this case, the pre-trigger will run before the item is created. Pre-triggers cannot have any input parameters. If necessary, the request object can be used to update the document body from original request. When triggers are registered, users can specify the operations that it can run with. If a trigger was created with `TriggerOperation.Create`, this means using the trigger in a replace operation will not be permitted. For examples, see the [How to write triggers article](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#pre-triggers).

* [Post-triggers](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#post-triggers)
<br>Similar to pre-triggers, post-triggers, are also associated with an operation on an Azure Cosmos item and they do not require any input parameters. They run after the operation has completed and have access to the response message that is sent to the client. For examples, see the [How to write triggers article](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#post-triggers).

### **Azure Functions trigger for Cosmos DB**
This section is relative to using the [Azure Functions trigger for Cosmos DB](https://docs.microsoft.com/azure/azure-functions/functions-bindings-cosmosdb-v2-trigger).

**Important:** Always make sure you are running the latest version of the [Azure Cosmos DB Extension package for Functions](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-changefeed-functions#dependencies)  

### **Function not receiving any or partial set of changes**  

**Availability**
<br>The Azure Functions trigger for Cosmos DB currently reads the Change Feed through the *Core (SQL) API*, that means that Mongo, Cassandra, and Table accounts are not yet supported.  

**Connectivity**
<br>Verify that your Azure Cosmos account's [Firewall configuration](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall) has Azure datacenters enabled or the Virtual Network your Function App is associated with (in case you are working with [App Service or Premium Plan](https://docs.microsoft.com/azure/azure-functions/functions-scale#hosting-plan-support)), whitelisted.  

**Error handling**
<br>The Azure Functions trigger for Cosmos DB, by default, *won't retry* a batch of changes if there was an unhandled exception during your code execution. This means that, if not handled correctly, when a batch of changes is received by your Function, execution can be stopping and inherently losing part of the batch. Make sure your Function's code has try/catch blocks, especially within any loop, to make sure that any failure in processing one document, does not exit the loop.  

**Multiplicity**
<br>The most common scenario, once connectivity and availability problems have been ruled out, is having multiple Azure Functions listening to the *same Monitored Collection* and using the *same Lease Collection*. When two or more Triggers share the same monitored and lease collection, the locking and load balancing algorithm will probably let one of them own the leases, while leaving the other Function out. This is expected, as these configurations should not be duplicated in multiple Triggers.
* If you want multiple Triggers to work independently, listening for changes in the same Monitored Collection, and also share the same Lease Collection for cost optimizations, you need to [configure them with different Prefixes](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-cosmos-db-trigger-logs)
* If you are unsure or don't know about extra Azure Functions running but you know how many Azure Function App instances you have running, you can inspect your Lease Collection and count the number of lease documents within, the distinct values of the *Owner* property in them should be equal to the number of instances of your Function App. If there are more Owners than the known Azure Function App instances, it means that these extra owners are the one "stealing" the changes. In that case, you can mitigate the situation by [configuring a different Prefix](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-cosmos-db-trigger-logs)  

### **Delay in receiving changes**
The rate at which the changes are delivered to your Function depends greatly on the speed at which your Function processes each batch. If the rate at which the changes are happening in the Monitored Collection is greater than the rate at which your Function processes them, there will be an increasing lag.  

1. Is your Azure Function deployed in the same region as your Azure Cosmos account? For optimal network latency, both the Azure Function and your Azure Cosmos account should be colocated in the same Azure region.
2. Are the changes happening in your Azure Cosmos container continuous or sporadic? If it's the latter, there could be some delay between the changes being stored and the Azure Function picking them up. This is because internally, when the trigger checks for changes in your Azure Cosmos container and finds none pending to be read, it will sleep for a configurable amount of time (5 seconds, by default) before checking for new changes (to avoid high RU consumption). You can configure this sleep time through the *FeedPollDelay/feedPollDelay* setting in the [configuration](https://docs.microsoft.com/azure/azure-functions/functions-bindings-cosmosdb-v2-trigger?tabs=csharp#configuration) of your trigger (the value is expected to be in milliseconds).
3. Your Azure Cosmos container might be [rate-limited](https://docs.microsoft.com/azure/cosmos-db/request-units)
4. You can use the `PreferredLocations` attribute in your trigger to specify a comma-separated list of Azure regions to define a custom preferred connection order, in cases where your Azure Cosmos DB account has multiple regions.
5. Measure and [monitor the Function execution time](https://docs.microsoft.com/azure/azure-functions/functions-monitoring). The Azure Functions trigger can only send new changes to be processed after you are done processing the current batch of changes to maintain the order of the events. If your Function execution is taking several seconds, please follow the [Azure Functions Best Practices](https://docs.microsoft.com/azure/azure-functions/functions-best-practices) and optimize the Function.

### **PartitionKey must be supplied for this operation***
This error means that you are currently using a partitioned lease collection with an old extension dependency. To solve this issue you need to update to the latest [extension dependency version](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-changefeed-functions#dependencies). If you are running on Azure Functions V1 (using the `Microsoft.Azure.WebJobs.Extensions.DocumentDB` package), **you need to migrate to Azure Functions V2 or greater** and use `Microsoft.Azure.WebJobs.Extensions.CosmosDB` instead.

### **What happens on a Function restart?**
The Azure Cosmos DB trigger uses the lease collection to store the state and the latest processed point in time on the Change Feed. If your Function restarts or you manually stop it and start it at a later time, it will continue from the saved point in time and pick up the changes that happened after. Based on the behavior of the [Change Feed](https://docs.microsoft.com/azure/cosmos-db/change-feed), only the latest version of a document (in case a document received multiple changes) will be read.

### **Using the Azure Cosmos DB SDK in Azure Functions**
This section refers to using the Cosmos DB SDK to perform operations in the context of an Azure Function. 

### **Functions Host restart**  
[Azure Functions Host has limits](https://docs.microsoft.com/azure/azure-functions/functions-scale#service-limits) regarding the number of connections, memory utilization, and execution timeout.
<br>If the Host is restarting it could be related to a violation of one of these limits.
<br>In the case of the Cosmos DB SDK the most common cause is not using the client as a **singleton** instance. Valid options are:
1. Use a [static client](https://docs.microsoft.com/azure/azure-functions/manage-connections#static-clients) instance.
1. Leverage [Dependency Injection on Azure Functions](https://docs.microsoft.com/azure/azure-functions/functions-dotnet-dependency-injection) to initialize and reuse the same client instance.

### **401 - UnauthorizedException**
This error is often related to using an invalid authorization key or credential. 
1. Verify that the Key being used is valid. If you are reading the Key or Connection String from an external source, like Azure Key Vault, verify the information there is up to date.
1. If there was a recent key rotation on the account, ensure you went with the [recommended procedure](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data#key-rotation). When using any old or new key there is a window of time where the key might not be valid.

### **Other issues**
For any other issues, see the **SDK (SQL API) Issues - Error or unexpected result** problem type. Azure Functions is mainly the execution environment and there is a possibility of the issue being a generic SDK issue covered in the general troubleshooting.

## **Recommended Documents**

[Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs)
<br>Azure Cosmos DB provides language-integrated, transactional execution of JavaScript. When using the SQL API in Azure Cosmos DB, you can write stored procedures, triggers, and user-defined functions (UDFs) in the JavaScript language. You can write your logic in JavaScript that executed inside the database engine. You can create and execute triggers, stored procedures, and UDFs by using Azure portal, the JavaScript language integrated query API in Azure Cosmos DB or the Cosmos DB SQL API client SDKs.  

[How to register and use stored procedures, triggers, and user-defined functions in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs)
<br>The SQL API in Azure Cosmos DB supports registering and invoking stored procedures, triggers, and user-defined functions (UDFs) written in JavaScript. You can use the SQL API .NET, .NET Core, Java, JavaScript, Node.js, or Python SDKs to register and invoke the stored procedures. Once you have defined one or more stored procedures, triggers, and user-defined functions, you can load and view them in the Azure portal by using Data Explorer.  	

[How to configure and read the Azure Cosmos DB Trigger logs](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-cosmos-db-trigger-logs)
<br>This article describes how you can configure your Azure Functions environment to send the Azure Functions trigger for Cosmos DB logs to your configured monitoring solution.  

[Create multiple Azure Cosmos DB Triggers](https://docs.microsoft.com/azure/cosmos-db/how-to-create-multiple-cosmos-db-triggers)
<br>This article describes how you can configure multiple Azure Functions triggers for Cosmos DB to work in parallel and independently react to changes.  

[Diagnose and troubleshoot issues when using Azure Cosmos DB Trigger in Azure Functions](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-changefeed-functions)
<br>This article covers common issues, workarounds, and diagnostic steps, when you use the Azure Functions trigger for Cosmos DB.

[Troubleshoot issues when using Azure Cosmos DB .NET SDK](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the .NET SDK with Azure Cosmos DB SQL API accounts.  

[FAQ](https://docs.microsoft.com/azure/cosmos-db/faq#sql-api-faq)
<br>Frequently asked questions about Cosmos DB SQL API.  