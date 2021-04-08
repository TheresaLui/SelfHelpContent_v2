<properties
	pageTitle="SDK .NET - Error or unexpected result"
	description="SDK .NET - Error or unexpected result"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32783716"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-sql-net-java-error"
	displayOrder="411"
	category="SDK (SQL API) Issues"
	ownershipId="AzureData_AzureCosmosDB"
/>

# SDK - Error or unexpected result

Most users are able to resolve issues with .NET SDK by using the steps below. The Recommended Documents section includes additional information for troubleshooting scenarios.


## **Recommended Steps**

### **Use latest SDK versions and singleton client**
Always make sure you're using the latest SDK:
* [Azure Cosmos DB .NET SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet-standard)
<br>Ensure that you are using a singleton client (one client instance for the lifetime of the application).

### **Known Issues and Solutions**
Review the GitHub issues listed in the following link for your SDK platform to see if there is a known bug, and to see the status of the fix from the Azure Cosmos DB team:  
* [.NET SDK](https://github.com/Azure/azure-cosmos-dotnet-v3/issues)

### **Retry logic**
Cosmos DB SDK on any IO failure will attempt to retry the failed operation if retry in the SDK is feasible. Having a retry in place for any failure is a good practice, and specifically, handling and retrying **write failures** is a must.

* Throttling errors (HTTP 429) are automatically retried by the SDK.
* Read and query IO failures are retried by the SDK without surfacing them to the end user.
* Writes (Create, Upsert, Replace, Delete) are **"not** idempotent and therefore, the SDK can't always blindly retry the failed write operations. The user's application logic must be able to handle the failure and retry.

### **Common Errors**  
  
**401: The MAC signature found in the HTTP request is not the same as the computed signature**
<br>The 401 error message, "The MAC signature found in the HTTP request is not the same as the computed signature," can be caused by the following scenarios:

* The key was rotated and did not follow the [best practices](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data#key-rotation). This is usually the case. Cosmos DB account key rotation can take anywhere from a few seconds to several days, depending on the Cosmos DB account size.
   * 401 MAC signature is seen shortly after a key rotation and eventually stops without any changes. 
* The key is misconfigured on the application so the key does not match the account.
   * 401 MAC signature issue will be consistent and happens for all calls.
* The application is using the [read-only keys](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data#master-keys).
   * 401 MAC signature issue will occur only when the application is doing write requests, but read requests will succeed.
* There is a race condition with container creation. An application instance is trying to access the container before container creation is complete. The most common scenario for this if the application is running, and the container is deleted and re-created with the same name while the application is running. The SDK will attempt to use the new container, but the container creation is still in progress, so it does not have the keys.
   * 401 MAC signature issue is seen shortly after a container creation, and only occur until the container creation is completed.


**403 Forbidden**
<br>The authorization token expired:  

* 403 is also returned during a POST to create a resource when the resource quota has been reached. Example: when a user tries to add documents to a collection that has reached its provisioned storage.
* 403 can also be returned when a stored procedure, trigger, or UDF has been flagged for high resource usage and blocked from execution.
* 403 forbidden error is returned when the firewall rules configured on your Azure Cosmos DB account block your request. Any requests originating from machines outside the allowed list will receive a 403 response. 
* 403.3 This status code is returned for write requests during the manual failover operation. This status code is used as redirection code by drivers to forward the writes to new write region. Direct REST client must perform GET on `DatabaseAccount` to identify the current write region and forward the write request to that endpoint.  


**429 Request rate too large**
<br>The volume of operations and data is higher than the provisioned throughput in the container. The service returns an HTTP 429 that tells the SDK to retry the operation after a time interval defined by the service. The SDK retries these errors 9 times by default.
* Setting `CosmosClientOptions.MaxRetryAttemptsOnRateLimitedRequests` to a different value to define how many retries you want to perform.
* Setting `CosmosClientOptions.MaxRetryWaitTimeOnRateLimitedRequests` to a different value to define the maximum period of time you want to retry for.

You should also consider either [increasing the provisioned throughput](https://docs.microsoft.com/azure/cosmos-db/set-throughput#update-throughput-on-a-database-or-a-container) or reducing the operational volume.


**449 Retry With**
<br>This is an expected response that indicates that there were concurrent operations trying to modify the same document. It is safe to retry. If the error is happening during stored procedure executions, decreasing the degree of parallelism of the executions will reduce the occurrence.


**404 NotFoundException: The read session is not available for the input session token**
<br>Update your SDK to a version higher than 2.12.0 if you're using the V2 SDK, or to 3.15.0 if using the V3 SDK.


**404 Not found**
<br>The HTTP status code 404 represents that the resource no longer exists.
* See [404 - not found](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-not-found).


**408 Request timeout or OperationCanceledException**
<br>The HTTP 408 or OperationCanceledException error occurs if the SDK was not able to complete the request before the timeout limit occurs. It often indicates that either the operation is taking longer to complete or that there are connectivity issues on the client environment.
* See [408 - request timeout](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk-request-timeout).

**SocketException**
<br>SocketExceptions are common on HTTP requests that are either taking longer than expected or facing connectivity issues between the instance and the final endpoint. Locally on the instance there should be a CPU usage verification and connection throttling/limiting investigation, any resource contention on both of these can be the source of the issue. Please also verify you are following the Singleton pattern and maintaining a single client for the lifetime of the application. Some environments (like Azure Kubernetes Service), could also impose limits on the established connections and such limits should be verified.
* See the [request timeout](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk-request-timeout) guide for details on verifying CPU and connection limiting.

**Intermittent 503 errors service is unavailable**
<br>This can be caused by transient connectivity issues on the client side or service availability.
* See [503 - service unavailable](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-service-unavailable)
* See [multiregional SDK availability](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-sdk-availability#transient-connectivity-issues-on-tcp-protocol)

**Invalid characters in Resource.Id _rid Property**
<br>Get request returns a bad request error may be given if the resource Id , _rid , property contains invalid characters.  
* The following characters are restricted and cannot be used in the Id property: */*, *\\*, *?*, *#* 
* See [Resource.Id Property](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.resource.id?view=azure-dotnet#remarks)  

**The read session is not available for the input session token**
<br>You receive an exception, "The read session is not available for the input session token."
* Newer SDK versions have improvements over this particular scenario.
* For a detailed explanation of the reason of this error code, see [this support article](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-sdk-availability#session-consistency-guarantees)

**IdleEndpointTimeout message from some connections Cosmos DB**
<br>This may occure if you aren't using the latest version of the [SDK](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet).  

**Stored procedure cannot insert due to partition key mismatch**
<br>`CancellationToken parameter` in `ExecuteStoredProcedureAsync` should be given as the third parameter. If it is not, the payload will be incorrect.  

**Error - Cross partition query is required but disabled. Please set `x-ms-documentdb-query-enablecrosspartition` to true, specify `x-ms-documentdb-partitionkey`, or revise your query to avoid this exception.**
<br>If your data was previously distributed using a single partition, your queries may have worked even though `EnableCrossPartitionQuery = false`. If your data is now distributed across more than one partition, enable the crossPartitionQuery by setting `enableCrossPartitionQuery=true` through the following code, to resolve the issue:  
`var option = new FeedOptions { EnableCrossPartitionQuery = true };`  

## **Recommended Documents**  

[Troubleshoot issues when using Azure Cosmos DB .NET SDK](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk)
<br>This article covers common issues, workarounds, diagnostic steps, and tools when you use the .NET SDK with Azure Cosmos DB SQL API accounts.  

[FAQ](https://docs.microsoft.com/azure/cosmos-db/faq#sql-api-faq)
<br>Frequently asked questions about Cosmos DB SQL API.  

[List of HTTP Status Codes for Azure Cosmos DB](https://docs.microsoft.com/rest/api/cosmos-db/http-status-codes-for-cosmosdb)
<br>This article provides the HTTP status codes returned by the REST operations.  

[How can I improve my database performance with .NET SDK?](https://docs.microsoft.com/azure/cosmos-db/performance-tips-dotnet-sdk-v3-sql)
<br>This article covers the most common improvements that will improve your application performance when using the .NET SDK.

