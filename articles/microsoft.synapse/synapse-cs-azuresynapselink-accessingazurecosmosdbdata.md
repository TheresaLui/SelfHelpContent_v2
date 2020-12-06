<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783834"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Azure Synapse Link/Accessing Azure Cosmos DB Data"
    description = "Azure Synapse Link/Accessing Azure Cosmos DB Data"
    articleId = "synapse-cs-azuresynapselink-accessingazurecosmosdbdata.md"
    ms.author = "saltug"
/>

# Azure Synapse Link/Accessing Azure Cosmos DB Data

Most users are able to resolve their Azure Synapse Link for Azure Cosmos DB issues using the steps below.  

## **Recommended Steps**  

### **Supported APIs**  

Today Azure Synapse Link for Azure Cosmos DB is supported for SQL API and Azure Cosmos DB API for MongoDB. It is not supported for Gremlin API and Table API. Support for Cassandra API is in private preview. For more information, contact the Azure Synapse Link team at cosmosdbsynapselink@microsoft.com.  


### **Unable to set item level TTL for data in analytical store**

At this time, TTL for analytical data can only be configured at container level and there is no support to set analytical TTL at item level.  

### **Unable to set container level TTL for data in analytical store**

At this time, when creating new containers, analytical TTL can be set for SQL API or MongoDB API containers.  

### **Updating the Analytical Store Time-To-Live**

After the analytical store is enabled with a particular TTL value, you can update it to a different valid value later. You can update the value by using the Azure portal or SDKs. For information on the various Analytical TTL config options, see [Analytical TTL supported values](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-ttl) article. Learn how to [configure Analytical TTL](https://docs.microsoft.com/azure/cosmos-db/configure-synapse-link#create-analytical-ttl).  

### **Unable to understand schema representation** 

There are two modes of schema representation in the analytical store. These modes have tradeoffs between the simplicity of a columnar representation, handling the polymorphic schemas, and simplicity of query experience:

- Well-defined schema representation (default for Azure Cosmos DB SQL API)
- Full fidelity schema representation (default for Azure Cosmos DB's API for MongoDB)  

Learn how to [automatically handle analytical store schemas](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-schema).  

### **Missing data (properties) in analytical store**

You can have a maximum of 200 properties at any nesting level in the schema, and a maximum nesting depth of 5. An item with 201 properties doesn't meet this constraint and it will not be represented in the analytical store. An item with more than 5 nested levels in the schema also doesn?t meet this constraint and it will not be represented in the analytical store.  

Another possible cause is: If the Azure Cosmos DB analytical store follows the well-defined schema representation and the specification above is violated by certain items, those items will not be included in the analytical store. Learn how to [automatically handle analytical store schemas](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-schema).  

### **Missing data (items or records or documents) in analytical store**

All transactional operations are propagated, including deletes. The analytical store TTL (time to live) setting also can cause data removal.

- If a document is deleted in transactional store, it will also be deleted from analytical store despite both stores ttls
- If transactional TTL is smaller than analytical TTL, the data is archived from transactional store but kept in analytical store up to the configured TTL limit
- If transactional TTL is bigger than analytical TTL, data will be archived from analytical store and kept in transactional store up to the configured TTL limit
- If you are using SQL API, it is well-defined schema by default, meaning that the first document in the collection will define the analytical store schema. Documents that violate that format won't be synced to the analytical store.  


### **Spark data is not refreshing**

In the case of **loading to Spark DataFrame**, the fetched metadata is cached through the lifetime of the Spark session. Therefore, subsequent actions invoked on the DataFrame are evaluated against the snapshot of the analytical store at the time of DataFrame creation.  

On the other hand, in the case of **creating a Spark table**, the metadata of the analytical store state is not cached in Spark and is reloaded on every Spark SQL query execution against the Spark table.  

Thus, you can choose between loading to Spark DataFrame and creating a Spark table based on whether you want your Spark analysis to be evaluated against a fixed snapshot of the analytical store or against the latest snapshot of the analytical store, respectively. [Learn more](https://docs.microsoft.com/azure/synapse-analytics/synapse-link/how-to-query-analytical-store-spark).  

## **Recommended Documents**  

[What is Azure Cosmos DB Analytical Store](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction)
<br>Azure Cosmos DB analytical store overview.  

[Analytical Store Time To Live (TTL) Overview](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#analytical-ttl)
<br>Analytical TTL indicates how long data should be retained in your analytical store, for a container.  

[Frequently asked questions about Synapse Link for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/synapse-link-frequently-asked-questions)
<br>This article answers commonly asked questions about Synapse Link for Azure Cosmos DB.  

[Schema Representation](https://docs.microsoft.com/azure/cosmos-db/analytical-store-introduction#schema-representation)  .
 