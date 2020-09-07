<properties
	pageTitle="Azure Cosmos DB Cassandra API feature support"
	description="Azure Cosmos DB Cassandra API feature support"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636830"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-cassandra-unsupported"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Apache Cassandra features Supported by Azure Cosmos DB Cassandra API

Azure Cosmos DB Cassandra API has the same syntax as Apache Cassandra and it supports a subset of Apache Cassandra features.

## **Recommended Steps**

You can communicate with the Cassandra API database through any of the open source Cassandra client drivers. The Cassandra API enables the use of existing client drivers by adhering to the Cassandra Query Language (CSQL) v4 wire protocol.

### **CQL Reserved Keywords**  
A reserved keyword such as *Password* cannot be used as an identifier unless you enclose the word in double quotation marks. Non-reserved keywords have a specific meaning in certain context but can be used as an identifier outside this context.
<br>Please see the CQL for Apache Cassandra reference [CQL Keywords](https://docs.datastax.com/en/archived/cql/3.3/cql/cql_reference/keywords_r.html) for a reserved keyword table and additional information.


## **Recommended Documents**
[Apache Cassandra features supported by Azure Cosmos DB Cassandra API](https://docs.microsoft.com/azure/cosmos-db/cassandra-support)
- Supported Cassandra Drivers
- Supported CQL data types and functions
- Cassandra API limits
- Tools
- CQLSH command-line utility and commands
- Usage of Cassandra retry connection policy
