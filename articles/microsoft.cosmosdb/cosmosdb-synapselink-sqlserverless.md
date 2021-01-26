<properties
	pageTitle="Azure Synapse Link for Cosmos DB - sqlserverless"
	description="Azure Synapse Link for Cosmos DB - sqlserverless"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32742615"
	resourceTags=""
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-sqlserverless"
	displayOrder="314"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>


# Azure Synapse Link for Azure Cosmos DB - SQL Serverless

Most users are able to resolve their Azure Synapse Link for Azure Cosmos DB issues using these steps.  


## **Recommended Steps**  

### **Supported APIs**  

Today Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview, for more information please contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.  

### **My query isn't showing the data I just inserted into Azure Cosmos DB Container**  

Azure Cosmos DB will sync your transactional data with analytical store within 2 and 5 minutes. Wait up to 5 minutes and re-run your query.


### **My query isn't working with the Linked Service for Azure Cosmos DB that I created**  

- Support for Linked Services is planned for the first half of 2021. Until then, use the `OPENROWSET` function.

- Try using Linked Services for Azure Cosmos DB containers with analytical store enabled.


### **Unable to load data into Cosmos DB using SQL Serverless**  

Synapse SQL Serverless is read only.  


### **Error when trying to create a view**  

Use an user database to create a view. You can't use the **master** or the **default** databases.

- If you try to create a view in the Synapse default database, you will get the error "Operation CREATE/ALTER VIEW is not allowed for a replicated database".

- If you try to create a view in the Synapse master database, you will get the error "CREATE/ALTER VIEW is not supported in master database".  


## **Recommended Documents**  

[Frequently asked questions about Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)  
<br>This article answers commonly-asked questions about Synapse Link for Azure Cosmos DB.  

[Query Azure Cosmos DB data with serverless SQL pool in Azure Synapse Link](https://docs.microsoft.com/azure/synapse-analytics/sql/query-cosmos-db-analytical-store)  
<br> This article has details and examples about Synapse SQL Serverless Pool for Synapse Link.

