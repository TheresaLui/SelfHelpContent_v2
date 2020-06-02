<properties
	pageTitle="Azure Synapse Link for Cosmos DB - TTL"
	description="Azure Synapse Link for Cosmos DB - TTL"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32742613"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-ttl"
	displayOrder="306"
	category="Azure Synapse Link for Cosmos DB TTL"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Synapse Link for Cosmos DB - Time To Live

Most users are able to resolve their Azure Synapse Link for Cosmos DB Time To Live (TTL) issue using the steps below.  



## **Recommended Steps**  


### **Updating the Analytical Store Time-To-Live**  
After the analytical store is enabled with a particular TTL value, you can update it to a different valid value later.  You can update the value by using the Azure portal or SDKs. See [Learn how to configure Analytical TTL](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link#create-analytical-ttl) 


### **Unable to set item level TTL for Analytical Store**  
At this time, TTL for analytical data can only be configured at container level and there is no support to set analytical TTL at item level.  



## **Recommended Documents**  

[Analytical TTL indicates how long data should be retained in your analytical store, for a container](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-ttl)
<br>For information on the various Analytical TTL config options.  

[Azure Synapse Link for Azure Cosmos DB supported features](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/concept-synapse-link-cosmos-db-support)
<br>This article describes the functionalities that are currently supported in Azure Synapse Link for Azure Cosmos DB.  

[Query Azure Cosmos DB Analytical Store with Apache Spark for Azure Synapse Analytics](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/how-to-query-analytical-store-spark)
<br>This article gives some examples on how you can interact with the analytical store from Synapse gestures. Gestures are visible when you right-click on a container. With gestures, you can quickly generate code and tailor it to your needs. Gestures are also perfect for discovering data with a single click.  

