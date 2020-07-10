<properties
	pageTitle="Azure Cosmos DB Cassandra API performance"
	description="Troubleshoot Azure Cosmos DB Cassandra API performance issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636817"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-cassandra-performance"
	displayOrder="145"
	category="Cassandra"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB Cassandra API Performance
Most users are able to resolve their Cassandra API performance issue using the steps below.

## **Recommended Steps**

### **High number of operations that are inserting or updating large documents in collection**

* Use smaller documents over larger ones
<br>Writing a 1kb document = 5 RUs, 4kb document = 7 RUs, 64kb document = 48 RUs. Therefore, use smaller documents when possible. If your data can be subdivided into parts that are updated independently, consider breaking it up into smaller documents.

* Evaluate encoding non-queryable content
<br>If there are properties/sections in your items that are not queried, but need to be globally distributed or accessed at low latency (e.g. binary content or free text), consider an encoding/compression to reduce their footprint and RU consumption.  

* Evaluate hybrid storage for binary content
<br>If there are properties/sections in your items that are not queried, and do not need to be globally distributed or accessed at low latency, consider moving them out to Blob Storage and store just the reference along with indexable metadata in Cosmos DB items.

* For data skews, consider the salting pattern
<br>If there are some keys with an uneven access pattern (e.g. super-users of your website who have a lot of activity events), consider the salting pattern so that their data can be spread across multiple partitions.



## **Recommended Documents**
[Provisioned throughput in Azure Cosmos DB Cassandra API](https://docs.microsoft.com/azure/cosmos-db/find-request-unit-charge#cassandra-api)
<br>When you perform operations against the Azure Cosmos DB Cassandra API, the RU charge is returned in the incoming payload as a field named RequestCharge. You have multiple options for retrieving the RU charge.