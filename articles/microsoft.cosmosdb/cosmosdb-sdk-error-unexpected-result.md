<properties
	pageTitle="SDK - Error or unexpected result"
	description="SDK - Error or unexpected result"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="resource"
	supportTopicIds="32688838"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-sdk-error-unexpected-result"
	displayOrder="284"
	category="SDK (SQL API) Issues"
/>

# Errors for SDK in Azure Cosmos DB

## **Recommended Steps**

Please check if you are on the [latest SDK version](https://www.nuget.org/packages/Microsoft.Azure.DocumentDB/)  


Review the Github issues links below for your SDK platform to see if there is a known bug, and status of the fix from the Azure Cosmos DB team.
* [.NET SDK](https://github.com/Azure/azure-cosmosdb-dotnet/issues)
* [Java SDK](https://github.com/Azure/azure-documentdb-java/issues)
* [Node.js SDK](https://github.com/Azure/azure-cosmos-js/issues)
* [Python SDK](https://github.com/Azure/azure-cosmos-python/issues)


**Common Errors**  
  


**403 Forbidden**
<br>
The authorization token expired.  

* 403 is also returned during a POST to create a resource when the resource quota has been reached. An example of this is when trying to add documents to a collection that has reached its provisioned storage.
* 403 can also be returned when a stored procedure, trigger, or UDF has been flagged for high resource usage and blocked from execution.
* 403 forbidden error is returned when the firewall rules configured on your Azure Cosmos DB account block your request. Any requests originating from machines outside the allowed list will receive a 403 response. 
* 403.3 – This status code is returned for write requests during the manual failover operation. This status code is used as redirection code by drivers to forward the writes to new write region. Direct REST client must perform GET on DatabaseAccount to identify the current write region and forward the write request to that endpoint.  

**429 Too Many Request**
<br>The collection has exceeded the provisioned throughput limit. Retry the request after the server specified retry after duration. 
<br>For more information, see [Handle rate limiting/request rate too large](https://docs.microsoft.com/azure/cosmos-db/performance-tips#throughput) and [Request Units](https://docs.microsoft.com/azure/cosmos-db/request-units)
  




## **Recommended Documents**

[How can I improve my database performance?](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>How a client connects to Azure Cosmos DB has important implications on performance, especially in terms of observed client-side latency. There are two key configuration settings available for configuring client Connection Policy – the connection mode and the connection protocol.
* Gateway mode
* Direct mode  


[FAQ](https://docs.microsoft.com/azure/cosmos-db/faq#sql-api)
<br>Frequently asked questions about Cosmos DB SQL API.  

[List of HTTP Status Codes for Azure Cosmos DB](https://docs.microsoft.com/rest/api/cosmos-db/http-status-codes-for-cosmosdb)
<br>This article provides the HTTP status codes returned by the REST operations.  
