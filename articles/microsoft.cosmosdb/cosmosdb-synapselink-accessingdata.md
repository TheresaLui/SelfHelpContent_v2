<properties
	pageTitle="Azure Synapse Link for Cosmos DB - accessingdata"
	description="Azure Synapse Link for Cosmos DB - accessingdata"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32742613,32743053"
	resourceTags=""
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-accessingdata"
	displayOrder="306"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Synapse Link for Cosmos DB - Accessing Data
Most users are able to resolve their Azure Synapse Link for Cosmos DB Accessing Data issue using the steps below.  


## **Recommended Steps**  

### **Unable to set item level TTL for Analytical Store**

At this time, TTL for analytical data can only be configured at container level and there is no support to set analytical TTL at item level. 

<br>

### **Updating the Analytical Store Time-To-Live**
After the analytical store is enabled with a particular TTL value, you can update it to a different valid value later. You can update the value by using the Azure portal or SDKs. For information on the various Analytical TTL config options, see [Analytical TTL supported values](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-ttl) article. Learn how to [configure Analytical TTL](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link#create-analytical-ttl). 

<br>

### **Missing items in Analytical Store** 
If specific items in your container violate the well-defined schema for analytics, they will not be included in the analytical store. If you have scenarios blocked by [well-defined schema for analytics](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-schema), please create a support ticket.  

<br>



## **Recommended Documents**  

[What is Azure Cosmos DB Analytical Store](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)
<br>Azure Cosmos DB analytical store overview.  

[Analytical Store Time To Live (TTL) Overview](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-ttl)
<br>Analytical TTL indicates how long data should be retained in your analytical store, for a container.  

[Frequently asked questions about Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>This article answers commonly asked questions about Synapse Link for Azure Cosmos DB.  
