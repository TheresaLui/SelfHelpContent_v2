<properties
	pageTitle="Azure Cosmos DB throttling"
	description="Azure Cosmos DB throttling"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="16"
	selfHelpType="resource"
	supportTopicIds="32597563,32597562"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Rate limiting in Azure Cosmos DB

Common reasons for rate limiting are:
* Insufficient RUs. 
* Skew within certain partitions or for specific time duration.
* Operations like scans or inserts of very large documents which are inefficient. 

Use the documents below to estimate your throughput needs and handle rate limiting effectively:


## **Recommended documents**
* [Estimating throughput needs](https://docs.microsoft.com/azure/cosmos-db/request-units#estimating-throughput-needs)
* [Exceeding reserved throughput limits](https://docs.microsoft.com/azure/cosmos-db/request-units#RequestRateTooLarge) 
* [Monitoring errors with Metrics](https://docs.microsoft.com/azure/cosmos-db/use-metrics#understanding-how-many-requests-are-succeeding-or-causing-errors)
* [Measuring and handling rate limiting errors](https://docs.microsoft.com/azure/cosmos-db/performance-tips#throughput)
