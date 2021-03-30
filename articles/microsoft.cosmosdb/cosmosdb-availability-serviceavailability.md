<properties
	pageTitle="Cosmos DB returns service unavailable"
	description="Troubleshoot Azure Cosmos DB Availability issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32681470"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-availability-serviceavailability"
	displayOrder="68"
	category="Core (SQL)"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Cosmos DB returns service unavailable

The Cosmos DB client will return the message "Service Unavailable" when client machine issues, service issues, or environment (network) issues occur. If this error occurs without an correlating service health issue in the Azure portal, the problem is likely due to high CPU, low memory, or network failure at the client level.

## **Recommended Steps**

### **Use latest SDK versions and singleton client**

* Always ensure that you are using the latest SDK, [Azure Cosmos DB .NET SDK for SQL API: Download and release notes](https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet-standard)
* Ensure you are using singleton client  

### **Firewall**

Failures related to blocked requests from a firewall can return an error, such as "Request originated from client IP {...} through public internet. This is blocked by your Cosmos DB account firewall settings." 

In these cases, make sure that your [firewall configuration](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall) includes the desired IP. If you recently modified this configuration, keep in mind that changes can take up to 15 minutes to propagate.

### **TransportException**
The "ServiceUnavailable" exception can contain a "TransportException" when the exception details are serialized. The TransportException normally indicates a client-side connectivity issue and returns an error, such as "TransportException: A client transport error occurred: The request timed out while waiting for a server response. 
(Time: xxx, activity ID: xxx, error code: ReceiveTimeout [0x0010], base error: HRESULT 0x80131500"

The TransportException can also contain a CPU history measurement, which takes a CPU utilization measurement every 10 seconds. For example:

```
CPU history: 
(2020-08-28T00:40:09.1769900Z 0.114), 
(2020-08-28T00:40:19.1763818Z 1.732), 
(2020-08-28T00:40:29.1759235Z 0.000), 
(2020-08-28T00:40:39.1763208Z 0.063), 
(2020-08-28T00:40:49.1767057Z 0.648), 
(2020-08-28T00:40:59.1689401Z 0.137), 
CPU count: 8)
```

- If the CPU measurements are over 70%, the ServiceUnavailable is likely to be caused by CPU exhaustion. In this case, the solution is to investigate the source of the high CPU utilization and reduce it, or scale the machine to a larger resource size.

- If the CPU measurements are not happening every 10 seconds (e.g., gaps or measurement times indicate larger times in between measurements), the cause is **thread starvation**. In this case the solution is to investigate the source/s of the thread starvation (potentially locked threads), or scale the machine/s to a larger resource size.

- If CPU measurements are normal, and the TransportException returns a request timeout, verify if the instance is running into **port exhaustion**. Depending on the service your application runs on, the metrics might differ. For instructions and next steps for the various Azure services, see [this article](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk-request-timeout#socket-or-port-availability-might-be-low).

**SocketException**
<br>SocketExceptions are common on HTTP requests that are either taking longer than expected or facing connectivity issues between the instance and the final endpoint. Locally on the instance there should be a CPU usage verification and connection throttling/limiting investigation, any resource contention on both of these can be the source of the issue. Verify that you are following the Singleton pattern and maintaining a single client for the lifetime of the application. Some environments (like Azure Kubernetes Service), can impose limits on the established connections. Such limits should also be verified.
* See the [request timeout](https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk-request-timeout) guide for details on verifying CPU and connection limiting.

### **Correlations**  

To collect multiple "ServiceUnavailableException" messages and determine if all failures involve a single machine or a single data replica, find the `StorePhysicalAddress` fields in the error messages.  

* **Example:** "ResponseTime: 2018-10-16T20:31:38.8084670Z, StoreReadResult: *StorePhysicalAddress: rntbd://dz5prdapp03-docdb-1.documents.azure.com:14135/*, LSN: -1, GlobalCommittedLsn: -1, PartitionKeyRangeId: , IsValid: True, StatusCode: 410, IsGone: True, IsNotFound: False, IsInvalidPartition: False, RequestCharge: 0, ItemLSN: -1, SessionToken: , ResourceType: Document, OperationType: Read"

If the message lacks a `StorePhysicalAddress` field, find the `Request URI` field.
* **Example:** "Microsoft.Azure.Documents.GoneException: Message: The requested resource is no longer available at the server. ActivityId: c3a37839-b476-4817-8a7a-a03ff0bca67d, *Request URI: /apps/905b0dc7-5521-445f-b54f-8e6e8fcddfba/services/bd39f580-9893-4671-bfa4-2ae279c8574a/partitions/84cf9e9f-9bfc-40d7-92eb-6268941dd0a3/replicas/131866380111007790s/*, RequestStats: , SDK: Microsoft.Azure.Documents.Common/2.1.0.0, Local IP: 100.115.170.28

If `TransportException` is present (.NET Cosmos DB SDK 2.3 and newer), find the `URI` and `connection` fields.
* **Example:** "Microsoft.Azure.Documents.TransportException: A client transport error occurred: The request timed out while waiting for a server response. (Time: 2019-01-09T09:47:10.7429304Z, activity ID: 960960f8-3191-4cc4-bd79-eff8028aaf59, error code: ReceiveTimeout [0x0010], base error: HRESULT 0x80131500, *URI: rntbd://byaprdapp05-docdb-2.documents.azure.com:14036/apps/2c77ff9f-6270-4ef5-9744-6cc65ce3cbc6/services/1222fe0d-54d5-43c0-8bcd-3343e7f7afde/partitions/191710da-2618-459f-8bc1-e806840c41fe/replicas/131894644130405731p/*, *connection: 10.90.123.166:64200 -> 40.118.245.251:14036*, payload sent: True, CPU history: not available, CPU count: 24)"

If multiple server host:port pairs or multiple (partition, replica) pairs are present across different error messages, this indicates a problem with the client machine with a high degree of confidence.  

If multiple client machines fail to connect to a single server, this may indicate a network or service issue. When filing a support ticket, include `StorePhysicalAddress`, `Request URI`, `server host:port`, and the `UTC time range` of the issue in your request.

### **Performance and Availability Tips**  
Ensure that your application follows the guidance outlined in this article:  
* [Performance Tips with respect to networking and SDKs](https://docs.microsoft.com/azure/cosmos-db/performance-tips-dotnet-sdk-v3-sql)

Additional latency and performance tips include:  
* Use [Direct/TCP as connectivity mode](https://docs.microsoft.com/azure/cosmos-db/sql-sdk-connection-modes)
* Include client into Cosmos account VNET 
* For Azure functions, use a non-consumption plan 
* Ensure that the Cosmos container is not getting throttled. By default, the SDK does retry throttles for availability, which you can override through the APIs below.
* Monitor physical resource utilization (CPU, memory, network throughput etc). Alert on excessive resource utilization.
* Use request deadlines appropriate for the service type: Shorter for latency-sensitive jobs (5-10 seconds) and longer for batch jobs (30-60 seconds)

### **Retry on failed operations**  
Retry failed operations:  
* [.NET Retry Options](https://docs.microsoft.com/dotnet/api/microsoft.azure.cosmos.cosmosclientoptions.maxretryattemptsonratelimitedrequests)
* [Java Retry Options](https://azure.github.io/azure-cosmosdb-java/1.0.0/index.html?com/microsoft/azure/cosmosdb/RetryOptions.html)
* Implement a retry loop with exponential back-off and random jitter for writes. Cosmos DB cannot automatically retry writes. 

## **Recommended Documents**  

[Performance tips for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
<br>This article describes how you can improve your database performance.  

[How to configure an IP firewall in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall)
<br>Learn how you can set an IP firewall on the Azure Cosmos DB account using the following:
* From the Azure portal
* Declaratively by using an Azure Resource Manager template
* Programmatically through the Azure CLI or Azure PowerShell by updating the `ipRangeFilter` property  

[Frequently Asked Questions: How to configure access from virtual networks (VNet)](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-vnet-service-endpoint)
<br>This article describes how to configure a virtual network service endpoint for an Azure Cosmos DB account, and provides answers to frequently asked questions.  

[IP firewall in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/firewall-support)
<br>This article provides an IP access control overview.
