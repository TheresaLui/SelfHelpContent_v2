<properties
	pageTitle="Gremlin system properties exposure"
	description="How to get system Cosmos DB properties exposed in gremlin"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="olignat"
	ms.author="olignat"
	selfHelpType="generic"
	supportTopicIds="32636756"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-gremlin-systemproperties"
/>
# Gremlin - System Cosmos DB Properties

Azure Cosmos DB has [system properties](https://docs.microsoft.com/en-us/rest/api/cosmos-db/databases) on every document ```_ts```, ```_self```, ```_attachments```, ```_rid``` and ```_etag```. Additionally, Graph engine adds ```inVPartition``` and ```outVPartition``` properties on edges. By default none of these properties are available for traversal. However, it is possible to include specific properties, or all of them, in Gremlin traversal.
```
g.withStrategies(ProjectionStrategy.build().IncludeSystemProperties('_ts').create())
```  
