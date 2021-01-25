<properties
	pageTitle="MongoDB Indexing"
	description="MongoDB Indexing"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32783714"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-mongod-indexing"
	displayOrder="225"
	category="MongoDB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Cosmos DB MongoDB Indexing 

Most users are able to resolve issues with MongoDB Indexing by using the steps below.


## **Recommended Steps**

### **Limitations**

Wildcard indexes don't support any of the following index types or properties:
- Compound
- TTL
- Unique

Unlike MongoDB, in Azure Cosmos DBs API for MongoDB, you can't use wildcard indexes for:

Creating a wildcard index that includes multiple specific fields

```
db.coll.createIndex( { "$**" : 1 }, { "wildcardProjection " : { "children.givenName" : 1, "children.grade" : 1 } } )
```

Creating a wildcard index that excludes multiple specific fields

```
db.coll.createIndex( { "$**" : 1 }, { "wildcardProjection" : { "children.givenName" : 0, "children.grade" : 0 } } )
```

As an alternative, you can create multiple wildcard indexes.

## **Recommended Documents**

[Manage indexing in Azure Cosmos DB API for MongoDB](https://docs.microsoft.com/azure/cosmos-db/mongodb-indexing)
<br>This article focuses on how to add indexes using Azure Cosmos DBs API for MongoDB.   

[Azure Cosmos DB MongoDB 3.6 Feature Support](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
<br>Azure Cosmos DB API for MongoDB *3.6 version* supported features and syntax.
