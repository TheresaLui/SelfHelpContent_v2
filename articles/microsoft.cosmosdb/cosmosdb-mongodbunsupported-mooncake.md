<properties
	pageTitle="MongoDB feature support"
	description="MongoDB feature support"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	ms.author="bharathb"
	selfHelpType="resource"
	supportTopicIds="32636831"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="MoonCake"
	articleId="cosmosdb-mongodbunsupported"
	displayOrder="46"
	category="MongoDB"
/>

# MongoDB API Support

Cosmos DB's API for MongoDB is compatible with MongoDB server version 3.2 by default. See [MongoDB Feature Support](https://docs.azure.cn/cosmos-db/mongodb-feature-support) for the list of supported operators and limitations. 

Features or query operators added in MongoDB version 3.4, including aggregation pipeline support is currently available as a preview feature. See [Mongo Preview Features](https://azure.microsoft.com/blog/azure-cosmosdb-extends-support-for-mongodb-aggregation-pipeline-unique-indexes-and-more/) for to enable these capabilities.

## **Recommended Steps**

* Review and enable preview feature via the Azure Portal, for example, Mongo Aggregation Pipeline, or Mongo 3.4 compatibility
* Rewrite query minus the unsupported operator, with client-side logic when required

## **Recommended Documents**

* [MongoDB Feature Support](https://docs.azure.cn/cosmos-db/mongodb-feature-support)
