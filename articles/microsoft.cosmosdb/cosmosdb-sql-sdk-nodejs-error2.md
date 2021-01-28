<properties
	pageTitle="SDK Node.js or javascript - Error or unexpected result"
	description="SDK Node.js or javascript - Error or unexpected result"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32783717"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-sql-sdk-nodejs-error2"
	displayOrder="421"
	category="SDK (SQL API) Issues"
	ownershipId="AzureData_AzureCosmosDB"
/>

# DK Node.js or javascript SDK - Error or unexpected result
Most users are able to resolve their Node.js or javascript SDK case using the steps below. The Recommended Documents section contain further information for more troubleshooting scenarios.


## **Recommended Steps**

### **Use latest SDK versions and singleton client**
Always ensure you are using the latest SDK:
* [Azure Cosmos DB Node.js SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-node)
<br>Please ensure you are using singleton (one client instance for the lifetime of the application) client.

### **Known Issues and Solutions**
Review the Github issues links below for your SDK platform to see if there is a known bug, and status of the fix from the Azure Cosmos DB team:  
* [Node.js SDK](https://github.com/Azure/azure-sdk-for-js/issues)


### **Common Errors**  
  
**401: The MAC signature found in the HTTP request is not the same as the computed signature**
<br>If you received the following 401 error message: "The MAC signature found in the HTTP request is not the same as the computed signature." It can be caused by the following scenarios.

* The key was rotated and did not follow the [best practices](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data#key-rotation). This is usually the case. Cosmos DB account key rotation can take anywhere from a few seconds to possibly days depending on the Cosmos DB account size.
   * 401 MAC signature is seen shortly after a key rotation and eventually stops without any changes. 
* The key is misconfigured on the application so the key does not match the account.
   * 401 MAC signature issue will be consistent and happens for all calls
* The application is using the [read-only keys](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data#master-keys).
   * 401 MAC signature issue will only happen when the application is doing write requests, but read requests will succeed.
* There is a race condition with container creation. An application instance is trying to access the container before container creation is complete. The most common scenario for this if the application is running, and the container is deleted and recreated with the same name while the application is running. The SDK will attempt to use the new container, but the container creation is still in progress so it does not have the keys.
   * 401 MAC signature issue is seen shortly after a container creation, and only occur until the container creation is completed.


**403 Forbidden**
<br>The authorization token expired:  

* 403 is also returned during a POST to create a resource when the resource quota has been reached. An example of this is when trying to add documents to a collection that has reached its provisioned storage.
* 403 can also be returned when a stored procedure, trigger, or UDF has been flagged for high resource usage and blocked from execution
* 403 forbidden error is returned when the firewall rules configured on your Azure Cosmos DB account block your request. Any requests originating from machines outside the allowed list will receive a 403 response. 
* 403.3 This status code is returned for write requests during the manual failover operation. This status code is used as redirection code by drivers to forward the writes to new write region. Direct REST client must perform GET on DatabaseAccount to identify the current write region and forward the write request to that endpoint.  


**429 Request rate too large**
<br>The collection has exceeded the provisioned throughput limit. Retry the request after the server specified retry after duration.
For more information, see [Handle rate limiting/request rate too large](https://docs.microsoft.com/azure/cosmos-db/performance-tips#throughput) and [Request Units](https://docs.microsoft.com/azure/cosmos-db/request-units). 
* See the dedicated support article for [429 - request rate too large](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-service-unavailable).


**404 Not found**
<br>The HTTP status code 404 represents that the resource no longer exists.
* See the dedicated support article for [404 - not found](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-not-found).


**Intermittent 503 errors service is unavailable**
<br>This can be caused by transient connectivity issues on the client side or service availability.
* See the dedicated support article for [503 - service unavailable](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-service-unavailable)
* See the dedicated support article for [multiregional SDK availability](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-sdk-availability#transient-connectivity-issues-on-tcp-protocol)


**The read session is not available for the input session token**
<br>You receive an exception *The read session is not available for the input session token*
* Newer SDK versions have improvements over this particular scenario.
* For a detailed explanation of the reason of this error code, see [this support article](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-sdk-availability#session-consistency-guarantees)

**Unable to connect to Cosmos DB Account from Java SDK (Async API) - Using SQL API**
<br>This is typically caused by issues with the SSL certificates. Please verify your certificates.  

**Stored procedure cannot insert due to partition key mismatch**
<br>CancellationToken parameter in ExecuteStoredProcedureAsync should be given as the 3rd parameter. If it is not the payload will be incorrect.  


**Error - Cross partition query is required but disabled. Please set x-ms-documentdb-query-enablecrosspartition to true, specify x-ms-documentdb-partitionkey, or revise your query to avoid this exception.**
<br>If your data was previously distributed using a single partition your queries may have worked even though *EnableCrossPartitionQuery = false*. If your data is now distributed across more than one partition, please enable the crossPartitionQuery by setting enableCrossPartitionQuery=true through code as shown below to resolve the issue.  
`var option = new FeedOptions { EnableCrossPartitionQuery = true };`  


## **Recommended Documents**  

[FAQ](https://docs.microsoft.com/azure/cosmos-db/faq#sql-api-faq)
<br>Frequently asked questions about Cosmos DB SQL API.  

[JavaScript query API in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/javascript-query-api)
<br>In addition to issuing queries using the SQL API in Azure Cosmos DB, the Cosmos DB server-side SDK provides a JavaScript interface for performing optimized queries in Cosmos DB Stored Procedures and Triggers.  

[List of HTTP Status Codes for Azure Cosmos DB](https://docs.microsoft.com/rest/api/cosmos-db/http-status-codes-for-cosmosdb)
<br>This article provides the HTTP status codes returned by the REST operations.  

