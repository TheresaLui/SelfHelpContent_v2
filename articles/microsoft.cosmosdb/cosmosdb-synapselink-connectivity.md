<properties
	pageTitle="Azure Synapse Link for Cosmos DB - connectivity"
	description="Azure Synapse Link for Cosmos DB - connectivity"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32743028"
	resourceTags=""
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-connectivity"
	displayOrder="308"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Synapse Link for Azure Cosmos DB - Connectivity  

Most users are able to resolve their Azure Synapse Link for Azure Cosmos DB issues using the following steps.  


## **Recommended Steps**  

### **Supported APIs**  

Today Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview, for more information please contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.  

### **Workspace with Managed Virtual Network**   
Azure Synapse Link for Azure Cosmos DB is currently not supported in workspace with Managed Vnet.   
We recommend creating a workspace without Managed Vnet to access Azure Synapse Link.  


### **Cannot access Cosmos DB analytical store with Synapse SQL dedicated pool**  
Only Synapse SQL serverless pool and Synapse Spark pool are currently supported. Synapse SQL dedicated pool is not supported.  


### **Cannot access Cosmos DB analytical store with Synapse Studio that is in another subscription**  

When trying to access Cosmos DB analytical store from a Synapse in other subscription, you may get the error "An error occurred while calling... responseBody = {'code':'Forbidden','message':'Request originated from client IP ... through public internet. This is blocked by your Cosmos DB account firewall settings...".

This error occurs because your IP address must be present in the firewall settings of the Cosmos account you want to access. [Follow these instructions](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall#allow-requests-from-global-azure-datacenters-or-other-sources-within-azure).


## **Recommended Documents**  

[Azure Synapse Link limits](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/concept-synapse-link-cosmos-db-support)
<br>This article describes the functionalities that are currently supported in Azure Synapse Link for Azure Cosmos DB.

[Configure your Cosmos DB Firewall](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall#allow-requests-from-global-azure-datacenters-or-other-sources-within-azure)  
<br> This article describes how to configure your Cosmos DB firewall for access from another subscription.  

