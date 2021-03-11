<properties
	pageTitle="Azure Synapse Link for Cosmos DB - accessingdata"
	description="Azure Synapse Link for Cosmos DB - accessingdata"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32742613"
	resourceTags=""
	productPesIds="15585,15818"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-synapselink-accessingdata"
	displayOrder="306"
	category="Azure Synapse Link for Cosmos DB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# FAQ for Azure Synapse Link for Azure Cosmos DB - accessing data

Most users can resolve issues in Azure Synapse Link for Azure Cosmos DB by applying these answers to frequently asked questions. 

## **Recommended Steps**  

### **Supported APIs**

Currently, Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview. For more information, contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.

### **Can I set item level TTL (time to live) for data in the analytical store?**
No. At this time, TTL for analytical data can be configured only at the container level. There is no support to set analytical TTL at the item level.

### **Why can't I set container level TTL for data in analytical store?**
Currently, when you create new containers, you can set analytical TTL for SQL API or MongoDB API containers.

### **Can I updating the Analytical Store TTL?**
After the analytical store is enabled to have a particular TTL value, you can update it to a different valid value later by using the Azure portal or SDKs. For information about the various Analytical TTL configuration options, see [Analytical TTL supported values](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-ttl). You can also learn how to [configure Analytical TTL](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link#create-analytical-ttl).  

### **What is schema representation?**
There are two modes of schema representation in the analytical store. These modes have tradeoffs between the simplicity of a columnar representation, handling the polymorphic schemas, and simplicity of query experience:
- Well-defined schema representation (default for Azure Cosmos DB SQL API)
- Full fidelity schema representation (default for Azure Cosmos DB's API for MongoDB)  

Learn how to [automatically handle analytical store schemas](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-schema).  

### **Why is there missing data (properties) in the analytical store?**

You can have a maximum of 200 properties at any nesting level in the schema, and a maximum nesting depth of five. An item that has 201 properties exceeds this limit and won't be represented in the analytical store. An item that has more than five nested levels in the schema also doesn’t meet this constraint and won't be represented in the analytical store.
Another possible cause is if the Azure Cosmos DB analytical store follows the well-defined schema representation and the specification given here is violated by certain items. In this situation, those items will not be included in the analytical store. Learn how to [automatically handle analytical store schemas](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-schema).

### **Why is data (items or records or documents) missing from the analytical store?**

All transactional operations are propagated, including deletes. The analytical store TTL setting can also cause data removal.
- If a document is deleted in the transactional store, it will also be deleted from the analytical store despite both stores TTLs
- If the transactional TTL is less than two minutes, the transactional data will almost certainly be archived before it is replicated to the analytical store.
- If the transactional TTL is less than five minutes but greater than two minutes, the transactional data will likely be archived before it is replicated to the analytical store.
- If the transactional TTL is less than the analytical TTL, the data is archived from the transactional store but kept in the analytical store up to the configured TTL limit.
- If the transactional TTL is greater than the analytical TTL, the data will be archived from the analytical store and kept in the transactional store up to the configured TTL limit.
- By default, SQL API is a well-defined schema. This means that the first document in the collection defines the analytical store schema. Document properties that violate that format won't be represented in the analytical store.


### **How do I access a specific region?**

Azure Cosmos DB is a globally distributed database system that lets you read and write data from the local replicas of your database. Azure Cosmos DB transparently replicates the data to all the regions that are associated with your Cosmos account.
If you turn on the analytical store for a globally distributed container or collection, you will have the analytical store in all of your regions. To access a specific region, add it to your connection string:

```
account=<database account name>;database=<database name>;region=<region name>;key=<database account master key>

```

### **Why is Spark data not refreshing?**

About the **loading to Spark DataFrame** message, the fetched metadata is cached throughout the lifetime of the Spark session. Therefore, later actions that are invoked on the DataFrame are evaluated against the snapshot of the analytical store at the time of DataFrame creation.
On the other hand, in the case of **creating a Spark table**, the metadata of the analytical store state is not cached in Spark but is reloaded on every Spark SQL query execution against the Spark table.
Therefore, you can choose between loading to Spark DataFrame and creating a Spark table based on whether you want your Spark analysis to be evaluated against a fixed snapshot of the analytical store or against the latest snapshot of the analytical store, respectively. [Learn more](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/how-to-query-analytical-store-spark).

### **Why am I receiving a "File cannot be opened" error?**
If you receive a "Failed to execute query. File... cannot be opened because it does not exist or is used by another process" error message, check your permissions on the Azure Data Lake Store that supports your Synapse workspace. For more information, see [this quickstar topic](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-workspace#create-a-synapse-workspace).


## **Recommended documents**  

[What is Azure Cosmos DB Analytical Store?](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)
<br>Azure Cosmos DB analytical store overview.  

[Analytical Time-To-Live (TTL) Overview](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-ttl)
<br>Analytical TTL indicates how long data should be retained in your analytical store, for a container.    

[Frequently asked questions about Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>This article answers commonly asked questions about Synapse Link for Azure Cosmos DB.  

[Schema representation](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#schema-representation)
<br>This article answers commonly asked questions about analytical store schema inferece.  

[Cosmos DB global data distribution](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
<br>This article helps you to understand Cosmos DB data distribution.