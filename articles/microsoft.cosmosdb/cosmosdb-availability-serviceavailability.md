<properties
	pageTitle="Cosmos DB returns service unavailable"
	description="Cosmos DB Service Unavailable"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms,ovplaton-msft"
	ms.author="balaks,ovplaton"
	selfHelpType="generic"
	supportTopicIds="32636804,32636827"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-availability-serviceavailability"
/>
# Cosmos DB returns service unavailable

The Cosmos DB client might return "Service Unavailable" due to client machine issues, service issues, or environment (network) issues. If you don't see a service health issue in Azure Portal, a common reason for seeing this error is high CPU, low memory, or network failure at the client.

## **Recommended Steps**

Please ensure that your application follows the guidance outlined in this article: [Performance Tips with respect to networking and SDKs](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking).

### Resource Utilization

Ensure that average CPU utilization measured at 10 second intervals stays under the recommended limits:

* 40% for latency-sensitive services.
* 55% for throughput services.
* 70-90% for best-effort, batch or streaming jobs.

Monitor physical resource utilization (CPU, memory, network throughput etc). Alert on excessive resource utilization.

Use request deadlines appropriate for the service type: Shorter for latency-sensitive jobs (5-10 seconds) and longer for batch jobs (30-60 seconds).

### Retries

Retry failed operations:

* Set [`ConnectionPolicy.RetryOptions`](https://docs.microsoft.com/en-us/dotnet/api/microsoft.azure.documents.client.connectionpolicy.retryoptions) for reads.
* Implement a retry loop with exponential back-off and random jitter for writes. Cosmos DB cannot retry writes automatically because they are not idempotent in general.

### Correlations

Collect multiple `ServiceUnavailableException` messages and determine if all failures involve a single machine or a single data replica.

Find the `StorePhysicalAddress` fields in the error messages. For example:

> ResponseTime: 2018-10-16T20:31:38.8084670Z, StoreReadResult: **StorePhysicalAddress: rntbd://dz5prdapp03-docdb-1.documents.azure.com:14135/**, LSN: -1, GlobalCommittedLsn: -1, PartitionKeyRangeId: , IsValid: True, StatusCode: 410, IsGone: True, IsNotFound: False, IsInvalidPartition: False, RequestCharge: 0, ItemLSN: -1, SessionToken: , ResourceType: Document, OperationType: Read

If the message lacks a `StorePhysicalAddress` field, find the `Request URI` field. For example:

> Microsoft.Azure.Documents.GoneException: Message: The requested resource is no longer available at the server. ActivityId: c3a37839-b476-4817-8a7a-a03ff0bca67d, **Request URI: /apps/905b0dc7-5521-445f-b54f-8e6e8fcddfba/services/bd39f580-9893-4671-bfa4-2ae279c8574a/partitions/84cf9e9f-9bfc-40d7-92eb-6268941dd0a3/replicas/131866380111007790s/**, RequestStats: , SDK: Microsoft.Azure.Documents.Common/2.1.0.0, Local IP: 100.115.170.28

If `TransportException` is present (.NET Cosmos DB SDK 2.3 and newer), find the `URI` and `connection` fields. For example:

> Microsoft.Azure.Documents.TransportException: A client transport error occurred: The request timed out while waiting for a server response. (Time: 2019-01-09T09:47:10.7429304Z, activity ID: 960960f8-3191-4cc4-bd79-eff8028aaf59, error code: ReceiveTimeout [0x0010], base error: HRESULT 0x80131500, **URI: rntbd://byaprdapp05-docdb-2.documents.azure.com:14036/apps/2c77ff9f-6270-4ef5-9744-6cc65ce3cbc6/services/1222fe0d-54d5-43c0-8bcd-3343e7f7afde/partitions/191710da-2618-459f-8bc1-e806840c41fe/replicas/131894644130405731p/**, **connection: 10.90.123.166:64200 -> 40.118.245.251:14036**, payload sent: True, CPU history: not available, CPU count: 24)

If multiple server host:port pairs or multiple (partition, replica) pairs are present across different error messages, this indicates a problem with the client machine with a high degree of confidence.

If multiple client machines fail to connect to a single server, this may indicate a network or service issue.

## **Recommended Documents**

* [Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
* [Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)
* [Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java)
