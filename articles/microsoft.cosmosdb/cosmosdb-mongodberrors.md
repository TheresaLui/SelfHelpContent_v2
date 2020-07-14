<properties
	pageTitle="MongoDB Errors"
	description="MongoDB Errors"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636778,32636789,32741536"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-mongodberrors"
	displayOrder="223"
	category="MongoDB"
	ownershipId="AzureData_AzureCosmosDB"
/>
# MongoDB - Commonly faced errors

## **Recommended Steps**

### **Client connection errors and socket timeout**  
Mongo client drivers use "connection pooling". Whenever a mongo client is initialized to a remote address, the driver establishes more than one connection. On the server side, Inactive/Idle TCP connections which are idle for more than 30 minutes are automatically closed by the Azure Cosmos DB Mongo server.  
Mongo drivers are unaware of when connections are torn down by the server and reuse of torn down connections by new requests causes socket/connection exceptions.  
Retry/reconnect on connection/socket exceptions.  

To avoid connectivity messages, you may want to change the connection string to set maxConnectionIdleTime to 1-2 minutes.
* Mongo driver: configure *maxIdleTimeMS=120000* 
* Node.JS: configure *socketTimeoutMS=120000*, *autoReconnect* = true, *keepAlive* = true, *keepAliveInitialDelay* = 3 minutes

Tear down TCP connections at the client.
* Configure the client to tear down TCP connections before Cosmos DB does

### **Request rate exceeded errors**
Some of the queries including aggregations require a large amount of processing. If the collection's throughput is not enough, you will see these errors. You can confirm this by going to the *Metrics* blade and selecting the *Throughput* tab for your collection. You can also evaluate if the queries can be optimized further by making effective use of the index.  

### **Request timeout errors**
While executing a query using the Mongo API for Cosmos DB, the request might timeout when there is large amount of data to be processed. Increasing the collection throughput would help mitigate this issue. You can also evaluate if the queries can be optimized further by making effective use of the index.  
If you are wanting to delete large amounts of data without impacting RU:
* Consider using TTL (Based on Timestamp): [Expire data with Azure Cosmos DB's API for MongoDB](https://docs.microsoft.com/azure/cosmos-db/mongodb-time-to-live)
* Use Cursor/Batch size to perform the delete. You can fetch a single document at a time and delete it through a loop. This would help you to slowly delete without impacting your production application.

### **MongoDB wire version issues**
Some versions of MongoDB drivers require the initial handshake include a minimum wire protocol version.  
* Accounts on server version 3.6, the drivers should work with no change required   
* Accounts on server version 3.2, if the driver throws an error related to the wire protocol version, try enabling the preview feature for wire protocol version 3.4 and appending an appName identifying the account to the connection string: &appName=@accountName@ 

### **ExceededMemoryLimit**
As a multi-tenant service, if you receive this error it means the operation has gone over the client's memory allotment. This error is specific to server version 3.2 and will not be encountered on accounts on server version 3.6.  
Steps to correct for version 3.2:
* Reduce the scope of the operation through more restrictive query criteria 
<br>Example: *db.getCollection('users').aggregate([{$match: {name: "Andy"}}, {$sort: {age: -1}}]))*  



## **Recommended Documents**  

[Azure Cosmos DB's API for MongoDB (3.6 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)
<br>The Azure Cosmos DB's API for MongoDB is compatible with MongoDB server version 3.6 by default for new accounts. The supported operators and any limitations or exceptions are listed in this article. Any client driver that understands these protocols should be able to connect to Azure Cosmos DB's API for MongoDB.  

[Azure Cosmos DB's API for MongoDB (3.2 version): supported features and syntax](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support)
<br>This article covers MongoDB version 3.2. The supported operators and any limitations or exceptions are listed in this article.  

[Connect a MongoDB application to Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/connect-mongodb-account)
<br>Learn how to connect your MongoDB app to an Azure Cosmos DB by using a MongoDB connection string. You can then use an Azure Cosmos database as the data store for your MongoDB app.
<br>This tutorial provides two ways to retrieve connection string information:
* The quick start method, for use with .NET, Node.js, MongoDB Shell, Java, and Python drivers
* The custom connection string method, for use with other drivers  

[Use Robo 3T with Azure Cosmos DB's API for MongoDB](https://docs.microsoft.com/azure/cosmos-db/mongodb-robomongo)
<br>This article will help you to add your Cosmos account to the Robo 3T connection manager.



