<properties
	  pageTitle="Cosmos DB returns service unavailable issue"
	  description="Cosmos DB returns service unavailable issue"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="8982b6e8-b04f-44fb-a951-204f99b0eea1"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Cosmos DB returns service unavailable issue

<!--issueDescription-->

Dear customer.

The Cosmos DB client might return "Service Unavailable" due to client machine issues, service issues, or environment (network) issues. If you don't see a service health issue in Azure Portal, a common reason for seeing this error is high CPU, low memory, or network failure at the client level.

## **Recommended Steps:**

### **Use latest SDK versions and singleton client**
* Always ensure you are using the latest SDK, [Azure Cosmos DB .NET SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet)
* Ensure you are using singleton client  

### **Performance and Availability Tips**  
Please ensure that your application follows the guidance outlined in this article:  
* [Performance Tips with respect to networking and SDKs](https://docs.microsoft.com/azure/cosmos-db/performance-tips)

Ensure that average CPU utilization measured at 10 second intervals stays under the recommended limits:
* 40% for latency-sensitive services
* 55% for throughput services
* 70-90% for best-effort, batch or streaming jobs

Additional latency and performance tips include:  
* Use [Direct/Tcp as connectivity mode](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking)
* Include client into Cosmos account VNET 
* For Azure functions, use non-consumption plan 
* Ensure that Cosmos container is not getting throttled. By default SDK does retry throttles for availability, which you can override through below APIs.
* Monitor physical resource utilization (CPU, memory, network throughput etc). Alert on excessive resource utilization.
* Use request deadlines appropriate for the service type: Shorter for latency-sensitive jobs (5-10 seconds) and longer for batch jobs (30-60 seconds)

### **Retry on failed operations**  
Retry failed operations:  
* [.NET Retry Options](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.connectionpolicy.retryoptions)
* [Java Retry Options](https://azure.github.io/azure-cosmosdb-java/1.0.0/index.html?com/microsoft/azure/cosmosdb/RetryOptions.html)
* Implement a retry loop with exponential back-off and random jitter for writes. Cosmos DB cannot retry writes automatically because they are not idempotent in general.

### **Correlations**  

Collect multiple *ServiceUnavailableException* messages and determine if all failures involve a single machine or a single data replica, find the *StorePhysicalAddress* fields in the error messages.  
* **Example:** ResponseTime: 2018-10-16T20:31:38.8084670Z, StoreReadResult: *StorePhysicalAddress: rntbd://dz5prdapp03-docdb-1.documents.azure.com:14135/*, LSN: -1, GlobalCommittedLsn: -1, PartitionKeyRangeId: , IsValid: True, StatusCode: 410, IsGone: True, IsNotFound: False, IsInvalidPartition: False, RequestCharge: 0, ItemLSN: -1, SessionToken: , ResourceType: Document, OperationType: Read

If the message lacks a *StorePhysicalAddress* field, find the *Request URI* field.
* **Example:** Microsoft.Azure.Documents.GoneException: Message: The requested resource is no longer available at the server. ActivityId: c3a37839-b476-4817-8a7a-a03ff0bca67d, *Request URI: /apps/905b0dc7-5521-445f-b54f-8e6e8fcddfba/services/bd39f580-9893-4671-bfa4-2ae279c8574a/partitions/84cf9e9f-9bfc-40d7-92eb-6268941dd0a3/replicas/131866380111007790s/*, RequestStats: , SDK: Microsoft.Azure.Documents.Common/2.1.0.0, Local IP: 100.115.170.28

If *TransportException* is present (.NET Cosmos DB SDK 2.3 and newer), find the *URI* and *connection* fields.
* **Example:** Microsoft.Azure.Documents.TransportException: A client transport error occurred: The request timed out while waiting for a server response. (Time: 2019-01-09T09:47:10.7429304Z, activity ID: 960960f8-3191-4cc4-bd79-eff8028aaf59, error code: ReceiveTimeout [0x0010], base error: HRESULT 0x80131500, *URI: rntbd://byaprdapp05-docdb-2.documents.azure.com:14036/apps/2c77ff9f-6270-4ef5-9744-6cc65ce3cbc6/services/1222fe0d-54d5-43c0-8bcd-3343e7f7afde/partitions/191710da-2618-459f-8bc1-e806840c41fe/replicas/131894644130405731p/*, *connection: 10.90.123.166:64200 -> 40.118.245.251:14036*, payload sent: True, CPU history: not available, CPU count: 24)

If multiple server host:port pairs or multiple (partition, replica) pairs are present across different error messages, this indicates a problem with the client machine with a high degree of confidence.  

If multiple client machines fail to connect to a single server, this may indicate a network or service issue. When filing a support ticket, include *StorePhysicalAddress*, *Request URI*, server host:port and the UTC time range of the issue in your request.


## **Recommended Documents**  

[Performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>This article describes how you can improve your database performance.  

[How to configure IP firewall in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall)
<br>Learn how you can set an IP firewall on the Azure Cosmos DB account using the following:
* From the Azure portal
* Declaratively by using an Azure Resource Manager template
* Programmatically through the Azure CLI or Azure PowerShell by updating the ipRangeFilter property  

[Frequently Asked Questions: How to configure access from virtual networks (VNet)](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-vnet-service-endpoint)
<br>This article describes how to configure a virtual network service endpoint for an Azure Cosmos DB account, and provides answers to frequently asked questions.  

[IP firewall in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/firewall-support)
<br>This article provides an IP access control overview.

Thank you.


<!--/issueDescription-->

