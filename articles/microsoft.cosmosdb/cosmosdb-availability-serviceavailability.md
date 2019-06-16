<properties
	pageTitle="Cosmos DB returns service unavailable"
	description="Cosmos DB Service Unavailable"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	ms.author="balaks"
	selfHelpType="generic"
	supportTopicIds="32636804,32636827"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-availability-serviceavailability"
/>
# Cosmos DB returns service unavailable

"Service unavailable" may be returned due to client issues, service issues, or environment (network) issues.  If you don't see a service health issue in Azure Portal, a common reason for seeing this error is due to high CPU, low memory, or network exhaustion at the client side. 

## **Recommended Steps**

Please ensure that your application follows the guidance outlined in this article: [Performance Tips with respect to networking and SDKs](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking). Also, review resource usage on the client machine to ensure that key resources such as CPU and memory have sufficient capacity.

## **Recommended Documents**

* [Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
* [Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)
* [Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java)
