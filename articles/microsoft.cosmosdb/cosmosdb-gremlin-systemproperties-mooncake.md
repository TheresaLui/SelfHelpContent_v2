<properties
	pageTitle="Gremlin system properties exposure"
	description="How to get system Cosmos DB properties exposed in gremlin"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="olignat"
	ms.author="olignat"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="cosmosdb-gremlin-systemproperties-mooncake"
	displayOrder="33"
	category="Gremlin (Graph)"
/>
# Gremlin - System Cosmos DB Properties

Azure Cosmos DB has [system properties](https://docs.microsoft.com/rest/api/cosmos-db/databases) such as ```_ts```, ```_self```, ```_attachments```, ```_rid``` and ```_etag``` on every document. Additionally, Gremlin engine adds ```inVPartition``` and ```outVPartition``` properties on edges. By default, none of these properties are available for traversal. However, it is possible to include specific properties, or all of them, in Gremlin traversal.

```
g.withStrategies(ProjectionStrategy.build().IncludeSystemProperties('_ts').create())
```

### **E-Tag**

This property is used for optimistic concurrency control. To ensure that vertex or edge is updated by a single writer the following pattern is recommended

```g.withStrategies(ProjectionStrategy.build().IncludeSystemProperties('_etag').create()).V('1').has('_etag', '"00000100-0000-0800-0000-5d03edac0000"').property('test', '1')```

### **TTL**

If collection has document expiration enabled and documents have ```ttl``` property set on them then this property will be available in Gremlin traversal as a regular vertex or edge property. There is no need to use ```ProjectionStrategy``` to enable TTL exposure.

Vertex created with the traversal below will be automatically deleted in **123 seconds**.

```g.addV('vertex-one').property('ttl', 123)```


## **Recommended Documents**

* [Cosmos DB Optimistic Concurrency](https://docs.azure.cn/cosmos-db/faq#how-does-the-sql-api-provide-concurrency)
* [Time to Live (TTL) in Azure Cosmos DB](https://docs.azure.cn/cosmos-db/time-to-live)
