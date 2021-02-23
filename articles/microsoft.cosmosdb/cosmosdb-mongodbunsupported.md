<properties
	pageTitle="MongoDB feature support"
	description="MongoDB feature support"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636831"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-mongodbunsupported"
	displayOrder="225"
	category="MongoDB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# MongoDB API Support  

The Azure Cosmos DB's API for MongoDB is compatible with the following versions for new accounts:

* [MongoDB Feature Support (4.0 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-40) for the list of supported operators and limitations
* [MongoDB Feature Support (3.6 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36) for the list of supported operators and limitations
* [MongoDB Feature Support (3.2 version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support) for the list of supported operators and limitations


## **Recommended Steps**  

### **Encountering an Unsupported Command**  
* Consider Migration to [MongoDB (3.6+ version)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-40)
* Review and enable preview feature via the Azure Portal, for example, Mongo Aggregation Pipeline, or Mongo 3.4 compatibility
* Rewrite query minus the unsupported operator, with client-side logic when required  

### **Count query cannot run on multiple shards**  
This error is thrown on legacy MongoDB version 3.2 accounts when running a CRUD (Create, Read, Update, Delete) command against a sharded collection and the shard key value is not specified in the command.  This issue is addressed for new Mongo accounts on 3.6+.  
If you are experiencing this issue and unable to migrate to 3.6+, please consider the following solution:
* Use a combination of Cursor and find to get the required count. Example, for every shard key value from the cursor, modify the find command to contain the shard key field and its value.


## **Recommended Documents**  
[Azure Cosmos DB's API for MongoDB (4.0 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-40)
<br>The supported operators and any limitations or exceptions are listed in this article. Any client driver that understands these protocols should be able to connect to Azure Cosmos DB's API for MongoDB.

[Azure Cosmos DB's API for MongoDB (3.6 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
<br>The supported operators and any limitations or exceptions are listed in this article. Any client driver that understands these protocols should be able to connect to Azure Cosmos DB's API for MongoDB.  

[Azure Cosmos DB's API for MongoDB (3.2 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support)
<br>This article covers MongoDB version 3.2. The supported operators and any limitations or exceptions are listed in this article.  

[Azure Lock Management](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources)
<br>As an administrator, you may need to lock a subscription, resource group, or resource to prevent other users in your organization from accidentally deleting or modifying critical resources. This article covers how to enable locks in the Portal and the intent for each lock type.




