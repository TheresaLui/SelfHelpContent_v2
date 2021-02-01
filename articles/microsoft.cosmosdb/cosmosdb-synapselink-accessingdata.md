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

# Azure Synapse Link for Azure Cosmos DB - Accessing Data  

Most users are able to resolve their Azure Synapse Link for Azure Cosmos DB issues using the steps below.  

## **Recommended Steps**  

### **Supported APIs**  

Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview. For more information, contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.  


### Unable to set item level TTL for data in analytical store

At this time, TTL for analytical data can only be configured at the container level. There is no support to set analytical TTL at the item level.  

### Unable to set container level TTL for data in analytical store

At this time, when creating new containers, analytical TTL can be set for SQL API or MongoDB API containers.  

### Updating the Analytical Store Time-To-Live

After the analytical store is enabled with a particular TTL value, you can update it to a different valid value later by using the Azure portal or SDKs. For information on the various Analytical TTL config options, see [Analytical TTL supported values](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-ttl) article. Learn how to [configure Analytical TTL](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link#create-analytical-ttl).  

### Unable to understand schema representation

There are two modes of schema representation in the analytical store. These modes have tradeoffs between the simplicity of a columnar representation, handling the polymorphic schemas, and simplicity of query experience:

- Well-defined schema representation (default for Azure Cosmos DB SQL API)
- Full fidelity schema representation (default for Azure Cosmos DB's API for MongoDB)  

Learn how to [automatically handle analytical store schemas](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-schema).  

### Missing data (properties) in analytical store

You can have a maximum of 200 properties at any nesting level in the schema, and a maximum nesting depth of 5. An item with 201 properties exceeds this limit and won't be represented in the analytical store. An item with more than 5 nested levels in the schema also doesn’t meet this constraint and won't be represented in the analytical store.  

Another possible cause is: If the Azure Cosmos DB analytical store follows the well-defined schema representation and the specification above is violated by certain items, those items will not be included in the analytical store. Learn how to [automatically handle analytical store schemas](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-schema).  

### Missing data (items or records or documents) in analytical store

All transactional operations are propagated, including deletes. The analytical store TTL (time to live) setting can also cause data removal.

- If a document is deleted in transactional store, it will also be deleted from analytical store despite both stores TTLs
- If transactional TTL is smaller than 2 minutes, it is almost guaranteed that the transactional data will be archived before it is replicated to the analytical store. 
- If transactional TTL is smaller than 5 minutes, but bigger than 2 minutes, there is a big chance that the transactional data will be archived before it is replicated to analytical store. 
- If transactional TTL is smaller than analytical TTL, the data is archived from transactional store but kept in analytical store up to the configured TTL limit
- If transactional TTL is bigger than analytical TTL, data will be archived from analytical store and kept in transactional store up to the configured TTL limit
- If you are using SQL API, it is well-defined schema by default, meaning that the first document in the collection will define the analytical store schema. Documents properties that violate that format won't be represented in analytical store.  


### Accessing a Specific Region  

Azure Cosmos DB is a globally distributed database system that allows you to read and write data from the local replicas of your database. Azure Cosmos DB transparently replicates the data to all the regions associated with your Cosmos account.

If you turn on analytical store for a globally distributed container or collection, you will have analytical store in all of your regions. To access a specific region, add it to your connection string: 

```
SQL
'account=<database account name>;database=<database name>;region=<region name>;key=<database account master key>'

```  

### Spark data is not refreshing

In the case of **loading to Spark DataFrame**, the fetched metadata is cached through the lifetime of the Spark session. Therefore, subsequent actions invoked on the DataFrame are evaluated against the snapshot of the analytical store at the time of DataFrame creation.  

On the other hand, in the case of **creating a Spark table**, the metadata of the analytical store state is not cached in Spark and is reloaded on every Spark SQL query execution against the Spark table.  

Thus, you can choose between loading to Spark DataFrame and creating a Spark table based on whether you want your Spark analysis to be evaluated against a fixed snapshot of the analytical store or against the latest snapshot of the analytical store, respectively. [Learn more](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/how-to-query-analytical-store-spark).  

### "File cannot be opened" Error

If you get the error "Failed to execute query. File .... cannot be opened because it does not exist or is used by another process", check your permissions on the Azure Data Lake Store that supports your Synapse Workspace. For more information, see [this quickstart](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-workspace#create-a-synapse-workspace).


## **Recommended Documents**  

[What is Azure Cosmos DB Analytical Store](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)
<br>Azure Cosmos DB analytical store overview.  

[Analytical Store Time To Live (TTL) Overview](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-ttl)
<br>Analytical TTL indicates how long data should be retained in your analytical store, for a container.  

[Frequently asked questions about Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>This article answers commonly asked questions about Synapse Link for Azure Cosmos DB.  

[Schema Representation](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#schema-representation)
<br>This article answers commonly asked questions about analytical store schema inferece.  

[Cosmos DB Global Data Distribution](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
<br>This article helps you to understand Cosmos DB data distribution.
