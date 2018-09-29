<properties
	pageTitle="Gremlin Authentication/Connectivity"
	description="Gremlin Authentication/Connectivity"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="21"
	selfHelpType="resource"
	supportTopicIds="32597491,32597501"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# Connecting and authenticating with Gremlin API

## **Recommended Steps**

### **Using the Azure Cosmos DB connection string**
When using the .NET SDK, you can find the connection string in the Azure Cosmos DB account Overview blade, under the URI property. The .NET SDK URI (ends with "documents.azure.com:443") is used to connect using the Microsoft.Azure.Graphs library. The same blade also shows the Gremlin Endpoint (ends with "gremlin.cosmosdb.azure.com:443") which is used to connect using the Gremlin.Net library.

For Java, Python, Node.js SDKs - use the Keys page to retrieve the endpoint and the connection string for your Gremlin endpoint.

## **Recommended Documents**
* [Connect to Gremlin Endpoint using .NET SDKs](https://docs.microsoft.com/azure/cosmos-db/create-graph-dotnet)
* [Connect to Gremlin Endpoint using Java SDKs](https://docs.microsoft.com/azure/cosmos-db/create-graph-java)
* [Connect to Gremlin Endpoint using Node.js SDKs](https://docs.microsoft.com/azure/cosmos-db/create-graph-nodejs)
* [Connect to Gremlin Endpoint using Python SDKs](https://docs.microsoft.com/azure/cosmos-db/create-graph-python)
