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

### **Unable to set item level TTL for analytical store**
At this time, TTL for analytical data can only be configured at container level and there is no support to set analytical TTL at item level. 

<br>

### **Unable to set container level TTL for analytical store**
At this time, analytical store ttl only can be enable for new SQL API and MongoDB API containers.

<br>

### **Updating the Analytical Store Time-To-Live**
After the analytical store is enabled with a particular TTL value, you can update it to a different valid value later. You can update the value by using the Azure portal or SDKs. For information on the various Analytical TTL config options, see [Analytical TTL supported values](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-ttl) article. Learn how to [configure Analytical TTL](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link#create-analytical-ttl). 

<br>

### **Unable to understand schema representation** 
There are two modes of schema representation in the analytical store. These modes have tradeoffs between the simplicity of a columnar representation, handling the polymorphic schemas, and simplicity of query experience:

* Well-defined schema representation (default for Azure Cosmos DB SQL API)
* Full fidelity schema representation (default for Azure Cosmos DB's API for MongoDB)

Learn how to [automatically handle analytical store schemas](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-schema). 

<br> 

### Missing data (properties) in analytical store
You can have a maximum of 200 properties at any nesting level in the schema, and a maximum nesting depth of 5. An item with 201 properties at the top level doesn’t satisfy this constraint and hence it will not be represented in the analytical store. An item with more than five nested levels in the schema also doesn’t satisfy this constraint and hence it will not be represented in the analytical store. 

<br>

### Missing data (items or records or documents) in analytical store
All transactional operations are propagated, including deletes. And analytical store ttl (time to live) setting also can cause data removal.

* If a document is deleted in transactional store, it will also be deleted from analytical store. Despite both stores ttl's.
* If transactional ttl is smaller than analytical ttl, the data is archived from transactional store but kept in analytical store until the configured ttl.
* If transaction ttl is bigger than analytical ttl, data will be archived from analytical store and kept in transactional store until the configured ttl limit.

<br>


## **Recommended Documents**  

[What is Azure Cosmos DB Analytical Store](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)
<br>Azure Cosmos DB analytical store overview.  

[Analytical Store Time To Live (TTL) Overview](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-ttl)
<br>Analytical TTL indicates how long data should be retained in your analytical store, for a container.  

[Frequently asked questions about Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>This article answers commonly asked questions about Synapse Link for Azure Cosmos DB.  
