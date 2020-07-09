<properties
	pageTitle="Cosmos DB metrics"
	description="Cosmos DB metrics"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636799,32741538,32684530,32692542"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-portal-metrics"
	displayOrder="262"
	category="Monitoring"
	ownershipId="AzureData_AzureCosmosDB"
/>


# Monitor Cosmos DB metrics
<br>Cosmos DB provides several metrics in the Azure Portal to help monitor the health of your Cosmos DB account including request volume, throughput utilization, and increase in storage growth.

## Recommended Steps

**MaxRU/s metric is being depricated. The recommended metric now is NormalizedRU.**  
Please check this doc https://docs.microsoft.com/en-us/azure/cosmos-db/monitor-normalized-request-units  



**Metrics show throttling (429) but chart shows consumed throughput doesn't exceed provisioned throughput**   

- Scenario: You are seeing throttling (429) in Metrics, but the Max consumed RU/s per partition key range chart shows you are not exceeding the provisioned throughput on your database or container.

    -  By default, the Azure Cosmos DB client SDKs for SQL API handle 429s by retrying up to 9 times or 30 seconds. These 429s may never be surfaced to your application, but will still be reflected in the portal metrics.
    - Stored procedures with heavy read or query operation may result in 429s, but may not show as exceeding the provisioned RU in the database or container
    - As a [best practice](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs), stored procedures should be used for write operations that require ACID transactions against a single partition key value. Perform read and query operations using the client SDKs for best performance and RU utilization.  
    

**Metrics show throttling (429) at account level, but no throttles for individual databases or containers**  

- Scenario: You are seeing throttles (429) when viewing the metrics at the account level (when Database(s) and Container(s) are filtered to ALL), but not seeing 429s when filtered to any individual database or container.

    - When performing a high volume of operations on resources using the RID identifier that result in 429s (as opposed to id property), these 429 will not appear when Metrics are filtered to the resource
    - To have these 429s appear in Metrics, use the id property when performing these operations  
    

**Metadata throttling**  

- Scenario: You are seeing high rate of throttling (429) in the System metrics tab, and want to know the cause

    - Metadata throttling can occur when you are performing a high volume of CRUD operations on databases or containers, such as listing databases/containers or querying for offers to see the current provisioned throughput
    - Increasing the RU of the database or container will have no impact and is not recommended
    - Instead, identify which client is issuing these operations and consider implementing a backoff policy to send these requests at a lower rate  
    


## **Recommended Documents**

[Monitoring and debugging with metrics in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/use-metrics)
<br>Azure Cosmos DB provides metrics for throughput, storage, consistency, availability, and latency. The Azure portal provides an aggregated view of these metrics. You can also view Azure Cosmos DB metrics from Azure Monitor API.  

[Azure Cosmos DB monitoring data reference](https://docs.microsoft.com/azure/cosmos-db/monitor-cosmos-db-reference)
<br>This article provides a reference of log and metric data collected to analyze the performance and availability of Azure Cosmos DB.   

[Monitor Cosmos DB with alerts](https://docs.microsoft.com/azure/cosmos-db/monitor-accounts)
<br>You can monitor your Azure Cosmos DB accounts in the Azure portal. For each Azure Cosmos DB account, a full suite of metrics is available to monitor throughput, storage, availability, latency, and consistency. Metrics can be reviewed on the Account page, the new Metrics page, or in Azure Monitor.
