<properties
	pageTitle="Azure Cosmos DB Cassandra API feature support"
	description="Azure Cosmos DB Cassandra API feature support"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32741537"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-cassandra-other"
	displayOrder="144"
	category="Cassandra"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Apache Cassandra features Supported by Azure Cosmos DB Cassandra API

Azure Cosmos DB Cassandra API has the same syntax as Apache Cassandra and it supports a subset of Apache Cassandra features.

## **Recommended Steps**

### **Unable to update Consistency as well as enable or disable multi-region writes**
With VNET enabled accounts, the selected user making changes to the account must have permissions on the VNET.
* Add the necessary permissions to the desired user to make changes or assign another user with the expected permissions to update the consistency 



## **Recommended Documents**
[FAQ for Azure Cosmos DB Cassandra API](https://docs.microsoft.com/azure/cosmos-db/faq#cassandra)
<br>Common questions regarding Azure Cosmos DB Cassandra API.  

[Apache Cassandra features supported by Azure Cosmos DB Cassandra API](https://docs.microsoft.com/azure/cosmos-db/cassandra-support)
- Supported Cassandra Drivers
- Supported CQL data types and functions
- Cassandra API limits
- Tools
- CQLSH command-line utility and commands
- Usage of Cassandra retry connection policy  
