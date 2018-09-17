<properties
	pageTitle="CosmosDB throttling"
	description="CosmosDB throttling"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="16"
	selfHelpType="resource"
	supportTopicIds="32597563,32597562"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Rate limiting in Azure Cosmos DB
To get predictable performance and avoid rate limiting errors, you need to reserve appropriate throughput(RUs) in units of 100 RU/second. Use the below documents to estimate your throughput needs and handle rate limiting effectively.

## **Recommended documents**
* [Estimating throughput needs](https://docs.microsoft.com/azure/cosmos-db/request-units#estimating-throughput-needs)
* [Exceeding reserved throughput limits](https://docs.microsoft.com/azure/cosmos-db/request-units#RequestRateTooLarge) 
* [Monitoring errors with Metrics](https://docs.microsoft.com/azure/cosmos-db/use-metrics#understanding-how-many-requests-are-succeeding-or-causing-errors)
* [Measuring and handling rate limiting errors](https://docs.microsoft.com/azure/cosmos-db/performance-tips#throughput)
