<properties
	pageTitle="Azure Cosmos DB throttling"
	description="Azure Cosmos DB throttling"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32675640"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-throttling"
	displayOrder="241"
	category="Throughput and Scaling"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Rate limiting in Azure Cosmos DB

## **Recommended Steps**

### **Cannot find the option to enable Autopilot?**  
Autopilot has been registered for all users. Autopilot can only be enabled while creating new databases and containers from the Azure Portal.
* Support for CLI and SDK is not yet available
* Support to enable autopilot mode on existing containers and databases is not yet available


### **Rate limiting: Increase RU/s**
You may have not provisioned enough RUs to meet your per-second request rates. The throughput (RUs) can be increased via the Azure portal, ARM template, PowerShell, Azure CLI or the Cosmos DB SDK.

* [Update throughput (RU/s) using ARM templates](https://docs.microsoft.com/azure/cosmos-db/resource-manager-samples)
* [Update throughput (RU/s) using PowerShell](https://docs.microsoft.com/azure/cosmos-db/scripts/powershell/sql/ps-sql-ru-update?toc=%2fpowershell%2fmodule%2ftoc.json)
* [Update throughput (RU/s) using Azure CLI](https://docs.microsoft.com/azure/cosmos-db/scripts/scale-collection-throughput-cli?toc=%2fcli%2fazure%2ftoc.json)
* [Update throughput (RU/s using .NET SDK)](https://docs.microsoft.com/azure/cosmos-db/set-throughput#update-throughput-on-a-database-or-a-container)

### **Rate limiting: Increase retries**  
If your application is not latency sensitive, you can keep the RUs fixed and increase the number of retries for the Cosmos DB client. For the core (SQL) API, this is available as a configuration in the native SDK when you instantiate the Cosmos DB client.

```csharp

// update retries (default is 10)
RetryOptions retryOptions = new RetryOptions
{
    MaxRetryAttemptsOnThrottledRequests = 15
};

ConnectionPolicy connectionPolicy = new ConnectionPolicy
{
    ConnectionMode = ConnectionMode.Direct,
    ConnectionProtocol = Protocol.Tcp,
    RetryOptions = retryOptions
};

DocumentClient client = new DocumentClient(new Uri(endpoint), key, connectionPolicy);

client.OpenAsync();

```

### **Rate limiting: Partition Key Choice**  
If your throughput utilization is low overall, but you still see rate limiting, you may have to review your partition key choice for skew. You can monitor your Azure Cosmos DB containers in the Azure portal to see if your requests are skewed to one or few partitions. If this is the cause of the rate limiting, you can migrate to a new container with near zero downtime using Change Feed.

* [Monitor throughput distribution across partitions](https://docs.microsoft.com/azure/cosmos-db/use-metrics#determine-the-throughput-distribution-across-partitions)
* [Partitioning strategy and provisioned throughput costs](https://docs.microsoft.com/azure/cosmos-db/optimize-cost-throughput#partitioning-strategy-and-provisioned-throughput-costs)
* [Partitioning in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partitioning-overview)
* [Real-world data modeling and partitioning example](https://docs.microsoft.com/azure/cosmos-db/how-to-model-partition-example)
* [Change Feed in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/change-feed)

### **Rate limiting: Write-heavy scenarios (429 Errors)**  
If your RU consumption is predominantly from writes, you may be able to reduce RU consumption by modeling as smaller documents, tuning indexing policy, or by writing in batches.  

How to calculate your batch size:  
Your batch size depends on how many Azure Function instances could be running. You can calculate this way - your throughput / max number of instances / 10KB document sizes /5 RU per 1K. The result is your batch size.  

For example:
<br>100,000 RU
<br>20 function app instances
<br>10 KB max document size x 5 RU per insert
<br>100,000 /20 / 10 / 5 = 100.   


* [Understand Request units in Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
* [Real-world data modeling and partitioning example](https://docs.microsoft.com/azure/cosmos-db/how-to-model-partition-example)
* [Exclude unused paths from indexing for faster writes](https://docs.microsoft.com/azure/cosmos-db/performance-tips#indexing-policy)
* [Bulk Executor Library](https://docs.microsoft.com/azure/cosmos-db/bulk-executor-overview)

### **Rate limiting: Read-heavy scenarios**  
If your RU consumption is predominantly from reads, you may be able to reduce RU consumption by tuning individual queries, lowering consistency level, or by reading in batches.

* [Understand Request units in Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
* [Get query execution metrics and analyze performance](https://docs.microsoft.com/azure/cosmos-db/profile-sql-api-query)
* [Tune query performance](https://docs.microsoft.com/azure/cosmos-db/sql-api-query-metrics)
* [Optimize reads and writes cost](https://docs.microsoft.com/azure/cosmos-db/optimize-cost-reads-writes)



## **Recommended Documents**

[Request Units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units#estimating-throughput-needs)
<br>With Azure Cosmos DB, you pay for the throughput you provision and the storage you consume on an hourly basis. Throughput must be provisioned to ensure that sufficient system resources are available for your Azure Cosmos database at all times.  

[Monitor and debug with metrics](https://docs.microsoft.com/azure/cosmos-db/use-metrics#understanding-how-many-requests-are-succeeding-or-causing-errors)
<br>This article walks through common use cases and how Azure Cosmos DB metrics can be used to analyze and debug these issues.  

[Measuring and handling rate limiting errors](https://docs.microsoft.com/azure/cosmos-db/performance-tips#throughput)
<br>Measure and tune for lower request units/second usage.  



