<properties
	pageTitle="Gremlin Development"
	description="Gremlin Development"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	displayOrder="20"
	selfHelpType="resource"
	supportTopicIds="32597514,32597540,32597498"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# Gremlin - How to develop apps to manage data in Gremlin API?

## **Recommended Steps**

### **Getting started**
You can use the Azure command-line interface (CLI), Azure PowerShell, or the Azure portal to create and access data from Azure Cosmos DB Gremlin API accounts.
After you create an account, you can access the graph databases within that account by using a Gremlin API service endpoint https://[YOUR_ACCOUNT].gremlin.cosmosdb.azure.com, that provides a WebSocket frontend for Gremlin.

You can configure your TinkerPop-compatible tools, like the Gremlin Console, to connect to this endpoint and build applications in Java, Node.js, or any Gremlin client driver.
During graph design, the decision of modelling an entity as a vertex of its own, as opposed to as a property of other vertex entities has performance and cost implications. The main driver for this decision relies on how the data is going to be queried, as well as the scalability of the model itself.

## **Recommended Documents**
* [Development using the Gremlin API](https://docs.microsoft.com/azure/cosmos-db/graph-introduction#get-started)
* [Supported Gremlin operators](https://docs.microsoft.com/azure/cosmos-db/gremlin-support)
