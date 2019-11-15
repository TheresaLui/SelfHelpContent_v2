<properties
	pageTitle="Funtion Triggers"
	description="Funtion Triggers"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="resource"
	supportTopicIds="32688843"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-function-triggers"
	displayOrder="66"
	category="Core (SQL)"
/>

# Troubleshooting function triggers

## **Recommended Steps**


### Triggers

Azure Cosmos DB supports two types of triggers:  

**Pre-triggers** 

[How to run pre-triggers](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#pre-triggers) 
Azure Cosmos DB provides triggers that can be invoked by performing an operation on an Azure Cosmos item. For example, you can specify a pre-trigger when you are creating an item. In this case, the pre-trigger will run before the item is created. Pre-triggers cannot have any input parameters. If necessary, the request object can be used to update the document body from original request. When triggers are registered, users can specify the operations that it can run with. If a trigger was created with TriggerOperation.Create, this means using the trigger in a replace operation will not be permitted. For examples, see How to write triggers article.
<br>

**Post-triggers**  

[How to run post-triggers](https://docs.microsoft.com/en-us/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs#post-triggers)
Similar to pre-triggers, post-triggers, are also associated with an operation on an Azure Cosmos item and they don’t require any input parameters. They run after the operation has completed and have access to the response message that is sent to the client. For examples, see How to write triggers article.
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




## **Recommended Documents**

* [Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs)  
Azure Cosmos DB provides language-integrated, transactional execution of JavaScript. When using the SQL API in Azure Cosmos DB, you can write stored procedures, triggers, and user-defined functions (UDFs) in the JavaScript language. You can write your logic in JavaScript that executed inside the database engine. You can create and execute triggers, stored procedures, and UDFs by using Azure portal, the JavaScript language integrated query API in Azure Cosmos DB or the Cosmos DB SQL API client SDKs.
<br>

* [How to register and use stored procedures, triggers, and user-defined functions in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-use-stored-procedures-triggers-udfs)  
The SQL API in Azure Cosmos DB supports registering and invoking stored procedures, triggers, and user-defined functions (UDFs) written in JavaScript. You can use the SQL API .NET, .NET Core, Java, JavaScript, Node.js, or Python SDKs to register and invoke the stored procedures. Once you have defined one or more stored procedures, triggers, and user-defined functions, you can load and view them in the Azure portal by using Data Explorer.
