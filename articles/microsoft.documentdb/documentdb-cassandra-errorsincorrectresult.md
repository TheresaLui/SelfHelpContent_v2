<properties
	pageTitle="Azure Cosmos DB Cassandra - Error or incorrect result"
	description="Cassandra - Error or incorrect result"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="408"
	selfHelpType="resource"
	supportTopicIds="32615111"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Azure Cosmos DB Cassandra API - Common errors

## **Recommended Steps**

### **Rate limiting errors**
Some of the queries including aggregations require a large amount of processing. If the collection's throughput is not enough, you will see these errors. You can confirm this by going to the [Metrics] blade and selecting the [Throughput] tab for your collection. You can review [Aggregate operations on Azure Cosmos DB Cassandra API tables from Spark](https://docs.microsoft.com/azure/cosmos-db/cassandra-spark-aggregation-ops) to perform aggregate operations.

### **SSL Connection failure**
Azure Cosmos DB enforces strick security requirements and does requires SSL for connection.
