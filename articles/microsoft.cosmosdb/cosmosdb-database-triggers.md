<properties
	pageTitle="Azure Cosmos DB Triggers"
	description="Configure Azure Cosmos DB Triggers"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636793"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-database-triggers"
	displayOrder="287"
	category="Tools and Connectors"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Functions trigger for Cosmos DB

## **Recommended Steps**

### **Database Triggers**
<br>*Note:*  Registered triggers do not run automatically when their corresponding operations (create / delete / replace / update) happen. They have to be explicitly called when executing these operations.  

Azure Cosmos DB supports two types of triggers:
* [Pre-triggers](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#pre-triggers)
<br>Azure Cosmos DB provides triggers that can be invoked by performing an operation on an Azure Cosmos item. For example, you can specify a pre-trigger when you are creating an item. In this case, the pre-trigger will run before the item is created. Pre-triggers cannot have any input parameters. If necessary, the request object can be used to update the document body from original request. When triggers are registered, users can specify the operations that it can run with. If a trigger was created with `TriggerOperation.Create`, this means using the trigger in a replace operation will not be permitted. For examples, see the [How to write triggers article](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#pre-triggers).

* [Post-triggers](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#post-triggers)
<br>Similar to pre-triggers, post-triggers, are also associated with an operation on an Azure Cosmos item and they do not require any input parameters. They run after the operation has completed and have access to the response message that is sent to the client. For examples, see the [How to write triggers article](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#post-triggers).

### **Azure Functions trigger**
If your issue is with the Azure Functions Trigger for Cosmos DB, please see the specific `Azure Functions Trigger` solution steps.

## **Recommended Documents**

[Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs)
<br>Azure Cosmos DB provides language-integrated, transactional execution of JavaScript. When using the SQL API in Azure Cosmos DB, you can write stored procedures, triggers, and user-defined functions (UDFs) in the JavaScript language. You can write your logic in JavaScript that executed inside the database engine. You can create and execute triggers, stored procedures, and UDFs by using Azure portal, the JavaScript language integrated query API in Azure Cosmos DB or the Cosmos DB SQL API client SDKs.  

[How to register and use stored procedures, triggers, and user-defined functions in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs)
<br>The SQL API in Azure Cosmos DB supports registering and invoking stored procedures, triggers, and user-defined functions (UDFs) written in JavaScript. You can use the SQL API .NET, .NET Core, Java, JavaScript, Node.js, or Python SDKs to register and invoke the stored procedures. Once you have defined one or more stored procedures, triggers, and user-defined functions, you can load and view them in the Azure portal by using Data Explorer.  	
