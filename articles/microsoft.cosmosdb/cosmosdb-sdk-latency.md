<properties 
	pageTitle="Azure Cosmos DB SQL API high latency" 
	description="Azure Cosmos DB SQL API high latency" 
	service="microsoft.documentdb" 
	resource="databaseAccounts" 
	authors="jimsch" 
	ms.author="jimsch" 
	selfHelpType="generic" 
	supportTopicIds="32688841,32688842,32688844"
	resourceTags="" 
	productPesIds="15585" 
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-sdk-latency"
	displayOrder="281"
	category="SDK Issues"
	ownershipId="AzureData_AzureCosmosDB"
/>

#  Azure Cosmos DB SQL API high latency issues  
Latency can happen due to application (threadpool, IO completion threads, etc...), machine (High CPU, low memory, etc...), environment (connectivity, cross-region, etc..) or Cosmos service issues.  
Latency sensitive applications are advised to use [performance tips](https://docs.microsoft.com/azure/cosmos-db/performance-tips). 

## **Recommended Steps**  

### **Use latest SDK versions and singleton client**  
Always ensure you are using the latest SDK, [Azure Cosmos DB .NET SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet). Cosmos SDK's are thread safe, ensure singleton client.  Co-locate the client application in the same Azure region as the Cosmos account. By default SDK will send all requests to the region the account was created in.  
<br>This can be overridden through below APIs:
* .NET V2 SDK DocumentClient [ConnectionPolicy.PreferredLocations](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.connectionpolicy.preferredlocations?view=azure-dotnet)
* .NET V3 SDK CosmosClient [CosmosClientOptions.ApplicationRegion](https://docs.microsoft.com/dotnet/api/microsoft.azure.cosmos.cosmosclientoptions.applicationregion?view=azure-dotnet)  

Additional latency and performance tips include:  
* Use [Direct/Tcp as connectivity mode](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking)
* Include client into Cosmos account VNET 
* For Azure functions, use non-consumption plan 
* Ensure that average CPU utilization measured at 10s stays under 40% 
* Ensure that Cosmos container is not getting throttled. By default SDK does retry throttles for availability, which can be overridden through below APIs.

### **Performance issues with Bulk Delete**  
Performance issue while deleting documents in Cosmos DB.
* Restructuring the code to query the partition ids and fetch all the documents in that partition which meet your criteria. Then run the delete on all the matching documents within that partition. This will avoid the cross partition queries and the performance will improve. 
* Also please see [Usage of Bulk support](https://github.com/Azure/azure-cosmos-dotnet-v3/tree/master/Microsoft.Azure.Cosmos.Samples/Usage/BulkSupport)


## **Recommended Documents**  

[Performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>This article describes how you can improve your database performance.  

[Troubleshoot issues when using Azure Cosmos DB .NET SDK](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the .NET SDK with Azure Cosmos DB SQL API accounts.  

[Troubleshoot issues when you use the Java Async SDK with Azure Cosmos DB SQL API accounts](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-java-async-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the Java Async SDK with Azure Cosmos DB SQL API accounts. The Java Async SDK provides client-side logical representation to access the Azure Cosmos DB SQL API. This article describes tools and approaches to help you if you run into any issues.  

[Cosmos DB .NET SDK on Github](https://github.com/Azure/azure-cosmos-dotnet-v2/issues)
<br>A list of known issues, workarounds, and SDK source code.  
