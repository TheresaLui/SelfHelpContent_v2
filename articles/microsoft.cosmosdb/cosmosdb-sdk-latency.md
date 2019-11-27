<properties 
	pageTitle="Azure Cosmos DB SQL API high latency" 
	description="Azure Cosmos DB SQL API high latency" 
	service="microsoft.documentdb" 
	resource="databaseAccounts" 
	authors="jimsch" 
	ms.author="jimsch" 
	selfHelpType="resource" 
	supportTopicIds="32688841,32688842,32688844"
	resourceTags="" 
	productPesIds="15585" 
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-sdk-latency"
	displayOrder="281"
	category="SDK Issues"
/>

#  Azure Cosmos DB SQL API high latency issues  
Latency can happen due to application (threadpool, IO completion threads, etc...), machine (High CPU, low memory, etc...), environment (connectivity, cross-region, etc..) or Cosmos service issues.  
Latency sensitive applications are advised to use [performance tips](https://docs.microsoft.com/azure/cosmos-db/performance-tips). 

## **Recommended Steps**  

### **Use latest SDK versions and singleton client**  
Always ensure you are using the latest SDK, [Azure Cosmos DB .NET SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet).  
Cosmos SDK's are thread safe, ensure singleton client.  Co-locate the client application in the same Azure region as the Cosmos account. By default SDK will send all requests to the region the account was created in.  
This can be overriden through below APIs:
* .NET V2 SDK DocumentClient [ConnectionPolicy.PreferredLocations](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.connectionpolicy.preferredlocations?view=azure-dotnet)
* .NET V3 SDK CosmosClient [CosmosClientOptions.ApplicationRegion](https://docs.microsoft.com/dotnet/api/microsoft.azure.cosmos.cosmosclientoptions.applicationregion?view=azure-dotnet)  

Additional latency and performance tips include:
* Use [Direct/Tcp as connectivty mode](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking)
* Include client into Cosmos account VNET 
* For Azure functions, use non-consumption plan 
* Ensure that average CPU utilization measured at 10s stays under 40% 
* Ensure that Cosmos container is not getting throttled. By default SDK does retry throttles for availability, which can be overriden through below APIs.


## **Recommended Documents**  

[Diagnose and troubleshoot issues when using Azure Cosmos DB .NET SDK](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the .NET SDK with Azure Cosmos DB SQL API accounts.  

[Performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>This article describes how you can improve your database performance.  

[Cosmos DB .NET SDK on Github](https://github.com/Azure/azure-cosmos-dotnet-v2/issues)
<br>A list of known issues, workarounds, and SDK source code.  
