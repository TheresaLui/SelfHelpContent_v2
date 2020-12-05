<properties 
	pageTitle="Azure Cosmos DB SDK .NET- Performance" 
	description="Azure Cosmos DB SDK .NET- Performance" 
	service="microsoft.documentdb" 
	resource="databaseAccounts" 
	authors="jimsch" 
	ms.author="jimsch" 
	selfHelpType="generic" 
	supportTopicIds="32783724"
	resourceTags="" 
	productPesIds="15585" 
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-sql-sdk-net-performance"
	displayOrder="413"
	category="SDK Issues"
	ownershipId="AzureData_AzureCosmosDB"
/>

#  Azure Cosmos DB SQL API high latency issues  
Latency can happen due to application (threadpool, IO completion threads, etc...), machine (High CPU, low memory, etc...), environment (connectivity, cross-region, etc..) or Cosmos service issues.  
Latency sensitive applications are advised to use [performance tips](https://docs.microsoft.com/azure/cosmos-db/performance-tips). 

## **Recommended Steps**  

### **Use latest SDK versions and singleton client**  
Always ensure you are using the latest SDK, [Azure Cosmos DB .NET SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet-standard). Cosmos SDKs are thread safe, ensure singleton client.  Co-locate the client application in the same Azure region as the Cosmos account. By default SDK will send all requests to the region the account was created in.  
<br>This can be overridden through below APIs:
* .NET V2 SDK DocumentClient [ConnectionPolicy.PreferredLocations](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.connectionpolicy.preferredlocations?view=azure-dotnet)
* .NET V3 SDK CosmosClient [CosmosClientOptions.ApplicationRegion](https://docs.microsoft.com/dotnet/api/microsoft.azure.cosmos.cosmosclientoptions.applicationregion?view=azure-dotnet)  

Additional latency and performance tips include:  
* Use [Direct/Tcp as connectivity mode](https://docs.microsoft.com/azure/cosmos-db/sql-sdk-connection-modes)
* Include client into Cosmos account VNET 
* For Azure functions, use non-consumption plan 
* Ensure that maximum CPU utilization measured at 10 second granularity stays under 40% 
* Ensure that Cosmos container is not getting throttled. By default SDK does retry throttles for availability, which can be overridden through below APIs.

### **Extract network diagnostic information**
The SDK provides detailed information on network latency on every request. You can obtain these details from:

* The *RequestDiagnosticsString* property on responses in .NET V2 SDK when using Direct connectivity mode.
* Calling `ToString()` on the *Diagnostics* property on responses and exceptions in .NET V3 SDK.

This valuable information will show which are the requests being done, and the network latency for each. This information is useful for the support team and can also be used to identify potential networking problems.


### **Ephemeral port exhaustion**
If you are facing a high connection volume or high port usage on your instances, first verify your client instances are singletons or unique for the lifetime of the application.
When running on the TCP protocol, the client optimizes for latency by using long-lived connections as opposed to HTTPS protocol, which terminates connections after 2 minutes of inactivity.

In scenarios where you have sparse access and you notice a higher connection count compared to Gateway mode you can:
* Configure [CosmosClientOptions.PortReuseMode on V3 SDK](https://docs.microsoft.com/dotnet/api/microsoft.azure.cosmos.cosmosclientoptions.portreusemode) or [ConnectionPolicy.PortReuseMode on V2 sdk](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.connectionpolicy.portreusemode) to **PrivatePortPool** (effective with framework version>= 4.6.1 and .net core version >= 2.0): This allows the SDK to use a small pool of ephemeral ports for different Cosmos DB destination endpoints.
* Configure [CosmosClientOptions.IdleConnectionTimeout on V3 SDK](https://docs.microsoft.com/dotnet/api/microsoft.azure.cosmos.cosmosclientoptions.idletcpconnectiontimeout) or [ConnectionPolicy.IdleConnectionTimeout on V2 SDK](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.connectionpolicy.idletcpconnectiontimeout)  with the values suggested in the documentation.


### **Performance issues with Bulk Delete**  
Performance issue while deleting documents in Cosmos DB.
* Restructuring the code to query the partition ids and fetch all the documents in that partition which meet your criteria. Then run the delete on all the matching documents within that partition. This will avoid the cross partition queries and the performance will improve. 
* Also please see [Usage of Bulk support](https://github.com/Azure/azure-cosmos-dotnet-v3/tree/master/Microsoft.Azure.Cosmos.Samples/Usage/BulkSupport)


## **Recommended Documents**  

[Performance tips for Azure Cosmos DB V2 SDK](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>This article describes how you can improve your database performance with .NET V2 SDK.  

[Performance tips for Azure Cosmos DB V3 SDK](https://docs.microsoft.com/azure/cosmos-db/performance-tips-dotnet-sdk-v3-sql)
<br>This article describes how you can improve your database performance with .NET V3 SDK. 

[Troubleshoot issues when using Azure Cosmos DB .NET SDK](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the .NET SDK with Azure Cosmos DB SQL API accounts.  

[Cosmos DB .NET SDK on Github](https://github.com/Azure/azure-cosmos-dotnet-v2/issues)
<br>A list of known issues, workarounds, and SDK source code.  
