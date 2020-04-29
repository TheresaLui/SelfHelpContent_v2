<properties
	pageTitle="Azure Cosmos DB Cassandra - Error or unexpected result"
	description="Cassandra - Error or unexpected result"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636787"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-cassandra-errorsincorrectresult"
	displayOrder="142"
	category="Cassandra"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB Cassandra API - Common errors

## **Recommended Steps**

### **Rate limiting errors**
Some of the queries including aggregations require a large amount of processing. If the collection's throughput is not enough, you will see these errors. You can confirm this by going to the **Metrics** blade and selecting the **Throughput** tab for your collection. 

### **SSL Connection failure**
Azure Cosmos DB enforces strict security requirements and does require SSL for connection.  

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

[Aggregate operations on Azure Cosmos DB Cassandra API tables from Spark](https://docs.microsoft.com/azure/cosmos-db/cassandra-spark-aggregation-ops)
<br>This article describes basic aggregation operations against Azure Cosmos DB Cassandra API tables from Spark.  

