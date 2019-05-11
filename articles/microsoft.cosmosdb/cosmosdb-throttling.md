<properties
	pageTitle="Azure Cosmos DB throttling"
	description="Azure Cosmos DB throttling"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	ms.author="bharathb"
	selfHelpType="generic"
	supportTopicIds="32636822"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="a675a3c4-3ea6-4b65-b52a-913cad37c231"
/>

# Rate limiting in Azure Cosmos DB

* You may have not provisioned enough RUs to meet your per-second request rates. The throughput (RUs) can be increased via the Azure portal or the Cosmos DB SDKs.
* If your application is not latency sensitive, you can keep the RUs fixed and increase the number of retries in your client application. For the core (SQL) API, this is available as a configuration in the native SDKs.
* If your throughput utilization is low overall, but you still see rate limiting, you may have to review your [partition key](https://docs.microsoft.com/azure/cosmos-db/partition-data) selection for skews. See [Synthetic partition keys](https://docs.microsoft.com/azure/cosmos-db/synthetic-partition-keys) for some solutions to deal with skews.
* If your RU consumption is predominantly from writes, you may be able to reduce RU consumption by modeling as smaller documents, tuning indexing policy, or by writing in batches. See [Request units](https://docs.microsoft.com/azure/cosmos-db/request-units) for details.
* If your RU consumption is predominantly from reads, you may be able to reduce RU consumption by tuning individual queries, lowering consistency level, or by reading in batches. See [Request units](https://docs.microsoft.com/azure/cosmos-db/request-units) for details.

## **Recommended Documents**

* [Estimating throughput needs](https://docs.microsoft.com/azure/cosmos-db/request-units#estimating-throughput-needs)
* [Exceeding reserved throughput limits](https://docs.microsoft.com/azure/cosmos-db/request-units#RequestRateTooLarge) 
* [Monitoring errors with Metrics](https://docs.microsoft.com/azure/cosmos-db/use-metrics#understanding-how-many-requests-are-succeeding-or-causing-errors)
* [Measuring and handling rate limiting errors](https://docs.microsoft.com/azure/cosmos-db/performance-tips#throughput)
