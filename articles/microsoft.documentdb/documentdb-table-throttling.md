<properties
	pageTitle="CosmosDB Table API throttling"
	description="CosmosDB Table API throttling"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="66"
	selfHelpType="resource"
	supportTopicIds="32597562"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>


# Rate Limitting or Throttling in Cosmos DB

The Cosmos DB collections are provisioned with a reserved throughput. The application would get a response code 429 (throttling) when the 
workload is consuming more then the provisioned throughput.  The request unit consumptions are evaluated on per second and the response 
contains the duration to wait before retyring the request. Use the below documents to estimate your throughput needs for a given 
workload or query.


## **Recommended documents**

* [Request units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
* [Estimating throughput needs](https://docs.microsoft.com/azure/cosmos-db/request-units#estimating-throughput-needs)
* [Request unit calculator](https://www.documentdb.com/capacityplanner)
* [Exceeding reserved throughput limits](https://docs.microsoft.com/azure/cosmos-db/request-units#RequestRateTooLarge) 
* [Set and get throughput for Azure Cosmos DB containers and database](https://docs.microsoft.com/azure/cosmos-db/set-throughput)
* [Partition and scale in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/partition-data)
