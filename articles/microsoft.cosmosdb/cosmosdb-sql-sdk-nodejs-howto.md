<properties 
	pageTitle="SDK Node.js or javascript - How to" 
	description="SDK Node.js or javascript - How to" 
	service="microsoft.documentdb" 
	resource="databaseAccounts" 
	authors="jimsch" 
	ms.author="jimsch" 
	selfHelpType="generic" 
	supportTopicIds="32783721"
	resourceTags="" 
	productPesIds="15585" 
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-sql-sdk-nodejs-howto" 
	displayOrder="422" 
	category="SDK Issues" 
	ownershipId="AzureData_AzureCosmosDB"
/>

# SDK Node.js or javascript - How to  
Most users are able to resolve their SDK Node.js or javascript case using the steps below. The Recommended Documents section contain further information for more troubleshooting scenarios.

## **Recommended Steps**  

### **Use latest SDK versions and singleton client**  
Always ensure you are using the latest SDK:
* [Azure Cosmos DB Node.js SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-node)
<br>Please ensure you are using singleton (one client instance for the lifetime of the application) client.

### **Known Issues and Solutions**  
Review the Github issues links below for your SDK platform to see if there is a known bug, and status of the fix from the Azure Cosmos DB team:
* [Node.js SDK](https://github.com/Azure/azure-sdk-for-js/issues)

### **Issues with Bulk Delete**
Performance issue while deleting documents in Cosmos DB.
* Restructuring the code to query the partition ids and fetch all the documents in that partition which meet your criteria. Then run the delete on all the matching documents within that partition. This will avoid the cross partition queries and the performance will improve. 
* Also please see [Usage of Bulk support](https://github.com/Azure/azure-cosmos-dotnet-v3/tree/master/Microsoft.Azure.Cosmos.Samples/Usage/BulkSupport)  

### **Is it advised to use both Pull (indexer) and Push (SDK) strategies on the same index?**
You can use both strategies but you should keep in mind that when indexer runs it will re-index the data based on the source so if push API is doing something differently than data source, indexer will overlap it or vice versa.
<br>If you are getting duplicated records, this may be due to the indexer will base64encode _rid, so if you base64encode and make sure that push API is getting same rid as indexer then you should not see duplicates. For additional information please see the following article [Create a target search index](https://docs.microsoft.com/azure/search/search-howto-index-cosmosdb#3---create-a-target-search-index)  



## **Recommended Documents**  

[Javascript Supported Functions](https://docs.microsoft.com/azure/cosmos-db/javascript-query-api#supported-javascript-functions)
<br>Cosmos DB server-side SDK provides a JavaScript interface for performing optimized queries in Cosmos DB Stored Procedures and Triggers.   

[Node.js examples to manage data in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/sql-api-nodejs-samples)
<br>Sample solutions that perform CRUD operations and other common operations on Azure Cosmos DB resources are included in the azure-cosmos-js GitHub repository. 
<br>This article provides:
- Links to the tasks in each of the Node.js example project files
- Links to the related API reference content  

[FAQ](https://docs.microsoft.com/azure/cosmos-db/faq#sql-api-faq)
<br>Frequently asked questions about Cosmos DB SQL API.  
