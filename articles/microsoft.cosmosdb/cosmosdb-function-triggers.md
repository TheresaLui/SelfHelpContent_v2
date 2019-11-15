<properties
	pageTitle="Azure Cosmos DB Triggers"
	description="Configure Azure Cosmos DB Triggers"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="resource"
	supportTopicIds="32636793,32688843"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-function-triggers"
	displayOrder="123"
	category="Tools and Connectors"
/>

# Azure Functions trigger for Cosmos DB

## Recommended Steps
Always make sure you are running the latest version of the [Azure Cosmos DB Extension package for Functions](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-changefeed-functions#dependencies).

### Triggers

Azure Cosmos DB supports two types of triggers:  

**Pre-triggers** 

[How to run pre-triggers](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#pre-triggers)   
Azure Cosmos DB provides triggers that can be invoked by performing an operation on an Azure Cosmos item. For example, you can specify a pre-trigger when you are creating an item. In this case, the pre-trigger will run before the item is created. Pre-triggers cannot have any input parameters. If necessary, the request object can be used to update the document body from original request. When triggers are registered, users can specify the operations that it can run with. If a trigger was created with TriggerOperation.Create, this means using the trigger in a replace operation will not be permitted. For examples, see How to write triggers article.
<br>

**Post-triggers**  

[How to run post-triggers](https://docs.microsoft.com/en-us/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#post-triggers)  
Similar to pre-triggers, post-triggers, are also associated with an operation on an Azure Cosmos item and they don�t require any input parameters. They run after the operation has completed and have access to the response message that is sent to the client. For examples, see How to write triggers article.
<br>

<table border="1" cellpadding="0" cellspacing="0" valign="top" style='direction:ltr;
 border-collapse:collapse;border-style:solid;border-color:#ffffff;border-width:
 1pt' title="" summary="">
 <tr>
  <td style='border-style:solid;border-color:#000000;border-width:1pt;
  background-color:#e2daf1;vertical-align:top;padding:2.0pt 3.0pt 2.0pt 3.0pt'>
  <p style='margin:0in;font-family:Calibri;font-size:14.0pt;color:#000000'>Note</p>
  Registered triggers don't run automatically when their corresponding operations (create / delete / replace / update) happen. They have to be explicitly called when executing these operations
  </td>
 </tr>
</table>


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




* [Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs)  
Azure Cosmos DB provides language-integrated, transactional execution of JavaScript. When using the SQL API in Azure Cosmos DB, you can write stored procedures, triggers, and user-defined functions (UDFs) in the JavaScript language. You can write your logic in JavaScript that executed inside the database engine. You can create and execute triggers, stored procedures, and UDFs by using Azure portal, the JavaScript language integrated query API in Azure Cosmos DB or the Cosmos DB SQL API client SDKs.


* [How to register and use stored procedures, triggers, and user-defined functions in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs)  
The SQL API in Azure Cosmos DB supports registering and invoking stored procedures, triggers, and user-defined functions (UDFs) written in JavaScript. You can use the SQL API .NET, .NET Core, Java, JavaScript, Node.js, or Python SDKs to register and invoke the stored procedures. Once you have defined one or more stored procedures, triggers, and user-defined functions, you can load and view them in the Azure portal by using Data Explorer.


* [How to configure and read the Azure Cosmos DB Trigger logs](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-cosmos-db-trigger-logs)  
This article describes how you can configure your Azure Functions environment to send the Azure Functions trigger for Cosmos DB logs to your configured monitoring solution.

* [Create multiple Azure Cosmos DB Triggers](https://docs.microsoft.com/azure/cosmos-db/how-to-create-multiple-cosmos-db-triggers)  
This article describes how you can configure multiple Azure Functions triggers for Cosmos DB to work in parallel and independently react to changes.

* [Diagnose and troubleshoot issues when using Azure Cosmos DB Trigger in Azure Functions](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-changefeed-functions)  
This article covers common issues, workarounds, and diagnostic steps, when you use the Azure Functions trigger for Cosmos DB.