<properties
	pageTitle="Azure Synapse Link for Cosmos DB - other"
	description="Azure Synapse Link for Cosmos DB - other"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32742614,32743056"
	resourceTags=""
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-other"
	displayOrder="318"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Synapse Link for Cosmos DB - My Issue is not Listed
Most users are able to resolve their Azure Synapse Link for Cosmos DB issue using the steps below.  


## **Recommended Steps**  

### **Experiencing latency when adding a new Cosmos DB region**
For multi-region Azure Cosmos DB accounts, the data stored in the analytical store is also globally distributed. Regardless of single write region or multiple write regions, analytical queries performed from Azure Synapse Analytics can be served from the closest local region.   
When planning to configure a multi-region Azure Cosmos DB account with analytical store support, it is recommended to have all the necessary regions added at time of account creation as if there is a large amounts of data this action can take a long time to complete.  

<br>

### **Picking a custom partitioning strategy for Analytical Store**
The data in analytical store is partitioned based on the horizontal partitioning of shards in the transactional store.  Currently, you cannot choose a different partitioning strategy for the analytical store.  

<br>

### **Synapse Link support for Azure Cosmos DB APIs**
In the public preview release, Synapse Link is supported only for the azure Cosmos DB SQL (Core) API.  Support for Azure Cosmos DB API for MongoDB and Cassandra is currently under gated preview.  To request access to gated preview, reach out to the Azure Cosmos DB Synapse Link team: *cosmosdbsynapselink@microsoft.com*  

<br>

### **Connecting to analytical store from analytics engines other than Azure Synapse Analytics**
You can only access and run queries against the analytical store using the various run-times provided by Azure Synapse Analytics. 
The analytical store can be queried and analyzed using:
* Synapse Spark with full support for Scala, Python, Spark SQL, and C#. Synapse Spark is central to data engineering and science scenarios 
* SQL serverless with T-SQL language and support for familiar BI tools (For example, Power BI Premium, etc.)  

<br>


## **Recommended Documents**  

[What is Azure Synapse Link for Azure Cosmos DB?](https://docs.microsoft.com/azure/cosmos-db/synapse-link)
<br> Synapse Link for Azure Cosmos DB  

[What is Azure Cosmos DB Analytical Store?](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)
<br>Azure Cosmos DB analytical store overview  

[Configure and use Azure Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link)
<br>Get started with Azure Synapse Link for Azure Cosmos DB  

[Azure Synapse Link for Azure Cosmos DB supported features](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/concept-synapse-link-cosmos-db-support)
<br>What is supported in Azure Synapse Analytics run time  

[Frequently asked questions about Azure Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>Frequently asked questions about Azure Synapse Link for Azure Cosmos DB  

[Azure Synapse Link for Azure Cosmos DB: Near real-time analytics use cases](https://docs.microsoft.com/azure/cosmos-db/synapse-link-use-cases)
<br>Azure Synapse Link for Azure Cosmos DB Use cases


