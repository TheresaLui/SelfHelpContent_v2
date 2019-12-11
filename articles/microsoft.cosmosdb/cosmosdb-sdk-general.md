<properties 
	pageTitle="Azure Cosmos DB SDK general" 
	description="Azure Cosmos DB SDK general" 
	service="microsoft.documentdb" 
	resource="databaseAccounts" 
	authors="jimsch" 
	ms.author="jimsch" 
	selfHelpType="generic" 
	supportTopicIds="32636812,32688840,32681010"
	resourceTags="" 
	productPesIds="15585" 
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-sdk-general" 
	displayOrder="290" 
	category="SDK Issues" 
/>

# Introduction to Azure Cosmos DB SDK  
Most users are able to resolve their .Net SDK case using the steps below.

## **Recommended Steps**  

### **Use latest SDK versions and singleton client**  
Always ensure you are using the latest SDK, [Azure Cosmos DB .NET SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet).
<br>Please ensure you are using singleton client.  

### **Known Issues and Solutions**  
Review the Github issues links below for your SDK platform to see if there is a known bug, and status of the fix from the Azure Cosmos DB team:    
* [.NET SDK](https://github.com/Azure/azure-cosmosdb-dotnet/issues)
* [Java SDK](https://github.com/Azure/azure-documentdb-java/issues)
* [Node.js SDK](https://github.com/Azure/azure-cosmos-js/issues)
* [Python SDK](https://github.com/Azure/azure-cosmos-python/issues)  

### **Issues with Bulk Delete**  
Performance issue while deleting documents in Cosmos DB.
* Restructuring the code to query the partition ids and fetch all the documents in that partition which meet your criteria. Then run the delete on all the matching documents within that partition. This will avoid the cross partition queries and the performance will improve. 
* Also please see [Usage of Bulk support](https://github.com/Azure/azure-cosmos-dotnet-v3/tree/master/Microsoft.Azure.Cosmos.Samples/Usage/BulkSupport)

## **Recommended Documents**  

[Diagnose and troubleshoot issues when using Azure Cosmos DB .NET SDK](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the .NET SDK with Azure Cosmos DB SQL API accounts.  

[Performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>This article describes how you can improve your database performance.  
