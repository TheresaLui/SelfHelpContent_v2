<properties
	pageTitle="Cosmos DB returns service unavailable"
  description="Cosmos DB Service Unavailable"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="86"
	selfHelpType="resource"
	supportTopicIds="32597558"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# Cosmos DB returns service unavailable

"Service unavailable" may be returned due to client issues, service issues, or environment (network) issues.  If you don't see a service health issue in Azure Portal, a common reason for seeing this error is due to high CPU, low memory, or network exhaustion at the client side. 

Please ensure that your application follows the guidance outlined in this article:[Performance Tips with respect to networking and SDKs](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking). Also, review resource usage on the client machine to ensure that key resources such as CPU and memory have sufficient capacity.

## **Recommended documents**

* [Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)
* [Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)
* [Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java)
