<properties
	pageTitle="SDK - Error or unexpected result"
	description="SDK - Error or unexpected result"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32688838,32688839"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-sdk-error-unexpected-result"
	displayOrder="284"
	category="SDK (SQL API) Issues"
/>

# SDK - Error or unexpected result
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


### **Common Errors**  
  
**403 Forbidden**
<br>The authorization token expired:  

* 403 is also returned during a POST to create a resource when the resource quota has been reached. An example of this is when trying to add documents to a collection that has reached its provisioned storage.
* 403 can also be returned when a stored procedure, trigger, or UDF has been flagged for high resource usage and blocked from execution
* 403 forbidden error is returned when the firewall rules configured on your Azure Cosmos DB account block your request. Any requests originating from machines outside the allowed list will receive a 403 response. 
* 403.3 This status code is returned for write requests during the manual failover operation. This status code is used as redirection code by drivers to forward the writes to new write region. Direct REST client must perform GET on DatabaseAccount to identify the current write region and forward the write request to that endpoint.  


**429 Too Many Requests**
<br>The collection has exceeded the provisioned throughput limit. Retry the request after the server specified retry after duration.
<br>For more information, see [Handle rate limiting/request rate too large](https://docs.microsoft.com/azure/cosmos-db/performance-tips#throughput) and [Request Units](https://docs.microsoft.com/azure/cosmos-db/request-units).  


**Invalid characters in Resource.Id _rid Property**
<br>Get request returns a bad request error may be given if the resource Id , _rid , property contains invalid characters.  
* The following characters are restricted and cannot be used in the Id property: */*, *\\*, *?*, *#* 
* Please see reference [Resource.Id Property](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.resource.id?view=azure-dotnet#remarks)  


**Date header doesn't conform to the required format**
<br>The Cosmos DB SDK has a dependency on joda-time lib 2.9.9.  Reference the Maven Artifact: [Java SDK for SQL API of Microsoft Azure Cosmos DB](https://mvnrepository.com/artifact/com.microsoft.azure/azure-documentdb/2.4.4). 
If you are using an older version of joda-time < 2.9.9 (maybe as a transitive dependency by another dependency) You may encounter this issue.
* Verify you are using the correct version of joda-time and explicitly setting the dependency for joda-time 2.9.9 will resolve the issue  


**The read session is not available for the input session token**
<br>You receive an exception *The read session is not available for the input session token*
* You need to upgrade your SDK version  


**Intermittent 503 errors service is unavailable**
<br>This can be caused by creating a new client and connection for each call to Cosmos DB which results in resource starvation. 
* Altering your code to use a singleton client should resolve the issue  


**Unable to connect to Cosmos DB Account from Java SDK (Async API) - Using SQL API**
<br>This is typically caused by issues with the SSL certificates. Please verify your certificates.  


**IdleEndpointTimeout message from some connections Cosmos DB**
<br>This may be caused if you are not using the latest version of the [SDK](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet).  


**Stored procedure cannot insert due to partition key mismatch**
<br>CancelationToken parameter in ExecuteStoredProcedureAsync should be given as the 3rd parameter. If it is not the payload will be incorrect.  


**Error - Cross partition query is required but disabled. Please set x-ms-documentdb-query-enablecrosspartition to true, specify x-ms-documentdb-partitionkey, or revise your query to avoid this exception.**
<br>If your data was previously distributed using a single partition your queries may have worked even though *EnableCrossPartitionQuery = false*. If your data is now distributed across more than one partition, please enable the crossPartitionQuery by setting enableCrossPartitionQuery=true through code as shown below to resolve the issue.  
'var option = new FeedOptions { EnableCrossPartitionQuery = true };'



## **Recommended Documents**  

[Troubleshoot issues when using Azure Cosmos DB .NET SDK](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the .NET SDK with Azure Cosmos DB SQL API accounts.  

[Troubleshoot issues when you use the Java Async SDK with Azure Cosmos DB SQL API accounts](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-java-async-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the Java Async SDK with Azure Cosmos DB SQL API accounts. The Java Async SDK provides client-side logical representation to access the Azure Cosmos DB SQL API. This article describes tools and approaches to help you if you run into any issues.  

[FAQ](https://docs.microsoft.com/azure/cosmos-db/faq#sql-api)
<br>Frequently asked questions about Cosmos DB SQL API.  

[List of HTTP Status Codes for Azure Cosmos DB](https://docs.microsoft.com/rest/api/cosmos-db/http-status-codes-for-cosmosdb)
<br>This article provides the HTTP status codes returned by the REST operations.  

[How can I improve my database performance?](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>How a client connects to Azure Cosmos DB has important implications on performance, especially in terms of observed client-side latency. There are two key configuration settings available for configuring client Connection Policy, the connection mode and the connection protocol.  
