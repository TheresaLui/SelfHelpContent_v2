<properties
	pageTitle="SDK Java- Error or unexpected result"
	description="SDK Java- Error or unexpected result"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32783715"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-sql-sdk-java-error"
	displayOrder="401"
	category="SDK (SQL API) Issues"
	ownershipId="AzureData_AzureCosmosDB"
/>

# SDK Java - Error or unexpected result
Most users are able to resolve issues with SQL SDK Java by using the steps below. The Recommended Documents section includes information for troubleshooting scenarios.


## **Recommended Steps**

### **Use latest SDK versions and a singleton client**
Always ensure you are using the latest SDK:
* [Azure Cosmos DB Java SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-java-v4)

<br>Make sure you are using a singleton client, which means one client instance for the lifetime of the application.

### **Known Issues and Solutions**
Review the Github issues links below for your SDK platform to see if there is a known bug, and to determine the status of the fix from the Azure Cosmos DB team:  
* [Java SDK](https://github.com/Azure/azure-sdk-for-java/issues)


### **Common Errors**  
  
**401: The MAC signature found in the HTTP request is not the same as the computed signature**
<br>The 401 error message, "The MAC signature found in the HTTP request is not the same as the computed signature," can be caused by one of the following scenarios:

* The key was rotated and did not follow the [best practices](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data#key-rotation). This is usually the case. Cosmos DB account key rotation can take anywhere from a few seconds to days, depending on the Cosmos DB account size.
   * 401 MAC signature is seen shortly after a key rotation and eventually stops without any changes. 
* The key is misconfigured on the application so the key does not match the account.
   * 401 MAC signature issue is consistent and happens for all calls.
* The application is using the [read-only keys](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data#master-keys).
   * 401 MAC signature issue will occur only when the application is doing write requests. Read requests will succeed.
* There is a race condition with container creation. An application instance is trying to access the container before container creation is complete. The most common scenario for this if the application is running, and the container is deleted and re-created with the same name while the application is running. The SDK will attempt to use the new container, but the container creation is still in progress so it does not have the keys.
   * 401 MAC signature issue occurs shortly after a container creation, and occurs only until the container creation is completed.


**403 Forbidden**
<br>The authorization token expired:  

* 403 is also returned during a POST to create a resource when the resource quota has been reached. Example: when you're trying to add documents to a collection that has reached its provisioned storage.
* 403 can also be returned when a stored procedure, trigger, or UDF has been flagged for high resource usage and blocked from execution.
* 403 forbidden error is returned when the firewall rules configured on your Azure Cosmos DB account block your request. Any requests originating from machines outside the allowed list will receive a 403 response. 
* 403.3 This status code is returned for write requests during the manual failover operation. This status code is used as a redirection code by drivers to forward the writes to new write region. Direct REST client must perform GET on DatabaseAccount to identify the current write region and forward the write request to that endpoint.  


**429 Request rate too large**
<br>The collection has exceeded the provisioned throughput limit. Retry the request after the server specified retry after duration.
For more information, see [Handle rate limiting/request rate too large](https://docs.microsoft.com/azure/cosmos-db/performance-tips#throughput) and [Request Units](https://docs.microsoft.com/azure/cosmos-db/request-units). 
* See the support article for [429 - request rate too large](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-service-unavailable).


**449 Retry With**
<br>This is an expected response that indicates that there were concurrent operations trying to modify the same document. It is safe to retry. If the error is happening during stored procedure executions, decreasing the degree of parallelism of the executions will also reduce the occurrence.


**404 Read session not available**
<br>Upgrade your SDK to the latest available version. This error has been fixed in newer SDK versions.


**404 Not found**
<br>The HTTP status code 404 represents that the resource no longer exists.
* See the support article for [404 - not found](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-not-found).


**Intermittent 503 errors service is unavailable**
<br>This can be caused by transient connectivity issues on the client side or service availability.
* See the support article for [503 - service unavailable](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-service-unavailable)
* See the support article for [multiregional SDK availability](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-sdk-availability#transient-connectivity-issues-on-tcp-protocol)


**Date header doesn't conform to the required format**
<br>The Cosmos DB SDK has a dependency on joda-time lib 2.9.9.  Reference the Maven Artifact: [Java SDK for SQL API of Microsoft Azure Cosmos DB](https://mvnrepository.com/artifact/com.microsoft.azure/azure-documentdb/2.4.4). 
<br>If you are using an older version of joda-time < 2.9.9 (maybe as a transitive dependency by another dependency) You may encounter this issue.
* Verify that you are using the correct version of joda-time. Explicitly setting the dependency for joda-time 2.9.9 will resolve the issue. 

**The read session is not available for the input session token**
<br>You receive the exception, "The read session is not available for the input session token"
* Newer SDK versions have improvements beyond this scenario.
* For a detailed explanation of this error code, see [this support article](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-sdk-availability#session-consistency-guarantees)


**Unable to connect to Cosmos DB Account from Java SDK (Async API) - Using SQL API**
<br>This is typically caused by issues with the SSL certificates. Please verify your certificates.   


**Stored procedure cannot insert due to partition key mismatch**
<br>CancellationToken parameter in ExecuteStoredProcedureAsync should be given as the 3rd parameter. If it is not, the payload will be incorrect.  

**Error - Cross partition query is required but disabled. Please set x-ms-documentdb-query-enablecrosspartition to true, specify x-ms-documentdb-partitionkey, or revise your query to avoid this exception.**
<br>If your data was previously distributed using a single partition your queries may have worked even though `EnableCrossPartitionQuery = false`. If your data is now distributed across more than one partition, enable the crossPartitionQuery by setting `enableCrossPartitionQuery=true`, as shown in the following code sample:

```
var option = new FeedOptions { EnableCrossPartitionQuery = true };  
```

## **Recommended Documents**  


[Troubleshoot issues when you use the Java SDK with Azure Cosmos DB SQL API accounts](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-java-sdk-v4-sql)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the Java V4 SDK with Azure Cosmos DB SQL API accounts.  

[FAQ](https://docs.microsoft.com/azure/cosmos-db/faq#sql-api-faq)
<br>Frequently asked questions about Cosmos DB SQL API.  

[List of HTTP Status Codes for Azure Cosmos DB](https://docs.microsoft.com/rest/api/cosmos-db/http-status-codes-for-cosmosdb)
<br>This article provides the HTTP status codes returned by the REST operations.  

[How can I improve my database performance with Java SDK?](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java-sdk-v4-sql)
<br>This article covers the most common improvements that will improve your application performance when using the Java SDK.
