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
When using the .NET SDKs, look at the Azure Cosmos DB Account overview page to retrieve the SDK URI string (looks like https://[YOUR-ACCOUNT].documents.azure.com:443/ and is used when you connect to the graph account by using Microsoft.Azure.Graphs library) and the Gremlin Endpoint (looks like https://[YOUR-ACCOUNT].gremlin.cosmosdb.azure.com:443/ and is used when you connect to the graph account by using Gremlin.Net library).
For Java, Python, Node.js SDKs - use the Keys page to retrieve the endpoint and the connection string for your Gremlin endpoint.

## **Recommended Documents**
* [Connect to Gremlin Endpoint using .NET SDKs](https://docs.microsoft.com/azure/cosmos-db/create-graph-dotnet)
* [Connect to Gremlin Endpoint using Java SDKs](https://docs.microsoft.com/azure/cosmos-db/create-graph-java)
* [Connect to Gremlin Endpoint using Node.js SDKs](https://docs.microsoft.com/azure/cosmos-db/create-graph-nodejs)
* [Connect to Gremlin Endpoint using Python SDKs](https://docs.microsoft.com/azure/cosmos-db/create-graph-python)
