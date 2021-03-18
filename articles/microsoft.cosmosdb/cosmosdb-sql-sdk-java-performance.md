<properties 
	pageTitle="SDK Java- Performance" 
	description="SDK Java- Performance" 
	service="microsoft.documentdb" 
	resource="databaseAccounts" 
	authors="jimsch" 
	ms.author="jimsch" 
	selfHelpType="generic" 
	supportTopicIds="32783723"
	resourceTags="" 
	productPesIds="15585" 
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-sql-sdk-java-performance"
	displayOrder="403"
	category="SDK Issues"
	ownershipId="AzureData_AzureCosmosDB"
/>

#  Azure Cosmos DB SQL API high latency issues  
Most users are able to resolve their Java SDK Performance issue with the following steps.

## **Recommended Steps**  

### **Use latest SDK versions and singleton client**  
* [Azure Cosmos DB Java SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-java-v4)

Additional latency and performance tips include:  
* Use [Direct/Tcp as connectivity mode](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking)
* Include client into Cosmos account VNET 
* For Azure functions, use non-consumption plan 
* Ensure that maximum CPU utilization measured at 10 second granularity stays under 40% 
* Ensure that Cosmos container is not getting throttled. By default SDK does retry throttles for availability, which can be overridden through below APIs.

### **Latency Issues**
Latency can happen due to application (threadpool, IO completion threads, etc...), machine (High CPU, low memory, etc...), environment (connectivity, cross-region, etc..) or Cosmos service issues.  
Latency sensitive applications are advised to use [Performance tips for Azure Cosmos DB Java SDK v4](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java-sdk-v4-sql?tabs=api-async).


### **Performance issues with Bulk Delete**  
Performance issue while deleting documents in Cosmos DB.
* Restructuring the code to query the partition ids and fetch all the documents in that partition which meet your criteria. Then run the delete on all the matching documents within that partition. This will avoid the cross partition queries and the performance will improve. 
* Also please see [Usage of Bulk support](https://github.com/Azure/azure-cosmos-dotnet-v3/tree/master/Microsoft.Azure.Cosmos.Samples/Usage/BulkSupport)


## **Recommended Documents**  


[Troubleshoot issues when you use the Java Async SDK with Azure Cosmos DB SQL API accounts](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-java-async-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the Java Async SDK with Azure Cosmos DB SQL API accounts. The Java Async SDK provides client-side logical representation to access the Azure Cosmos DB SQL API. This article describes tools and approaches to help you if you run into any issues.  
