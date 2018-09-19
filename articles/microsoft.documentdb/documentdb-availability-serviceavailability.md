<properties
	pageTitle="Cosmos DB returns Service Unavailable"
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
# Cosmos DB returns Service Unavailable

Service unavailable may be returned due to client issues, Service issues, or Environment (network) issues.  If you don't see a Service advisory in Azure portal, a common reason for seeing this error is from client load from CPU, Memory, or Network exhaustion at the client side. 

Please ensure the application has implemented the [Performance Tips with respect to Networking and SDKs](https://docs.microsoft.com/azure/cosmos-db/performance-tips#networking). Also, review the client resource such as CPU/Memory pressure on the client machine.

## **Recommended documents**

* [Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)

* [Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)

* [Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java)
