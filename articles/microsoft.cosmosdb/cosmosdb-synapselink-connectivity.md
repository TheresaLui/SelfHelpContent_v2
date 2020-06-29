<properties
	pageTitle="Azure Synapse Link for Cosmos DB - connectivity"
	description="Azure Synapse Link for Cosmos DB - connectivity"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32743028,32743055"
	resourceTags=""
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-connectivity"
	displayOrder="308"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Synapse Link for Cosmos DB - Connectivity
Most users are able to resolve their Azure Synapse Link for Cosmos DB Connectivity issue using the steps below.  


## **Recommended Steps**  

### **Workspace with Managed Virtual Network**   
Azure Synapse Link for Azure Cosmos DB is currently not supported in workspace with Managed Vnet.   

We recommend creating a workspace without Managed Vnet to access Azure Synapse Link. 

<br>

### **Cannot access Cosmos DB analytical store with Synapse SQL Serverless**  
Synapse SQL Serverless is currently under gated preview and not publicly available. To request access please email *cosmosdbsynapselink@microsoft.com*.   

<br>



## **Recommended Documents**  

[Azure Synapse Link limits](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/concept-synapse-link-cosmos-db-support)
<br>This article describes the functionalities that are currently supported in Azure Synapse Link for Azure Cosmos DB.
