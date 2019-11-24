<properties
	pageTitle="MongoDB Errors"
	description="MongoDB Errors"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="resource"
	supportTopicIds="32636778,32636789,32636810"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-mongodberrors"
	displayOrder="223"
	category="MongoDB"
/>
# MongoDB - Commonly faced errors

## **Recommended Steps**

### **Client connection errors and socket timeout**
Mongo client drivers use "connection pooling". Whenever a mongo client is initialized to a remote address, the driver establishes more than one connection. On the server side, Inactive/Idle TCP connections which are idle for more than 30 minutes are automatically closed down by the Azure Cosmos DB Mongo server.
<br>Mongo drivers are unaware of when connections are torn down by the server and reuse of torn down connections by new requests causes socket/connection exceptions.
<br>Clients can handle this in two ways:
* Retry/reconnect on connection/socket exceptions
<br>To avoid connectivity messages, you may want to change the connection string to set maxConnectionIdleTime to 1-2 minutes. Example: add the *maxIdleTimeMS=120000* at the end of your connection string
* Configure the client to tear down TCP connections before Cosmos DB does  

### **Request rate exceeded errors**
Some of the queries including aggregations require a large amount of processing. If the collection's throughput is not enough, you will see these errors. You can confirm this by going to the Metrics blade and selecting the Throughput tab for your collection. 
<br>You can also evaluate if the queries can be optimized further by making effective use of the index.  

### **Request timeout errors**
While executing a query using the Mongo API for CosmosDB, the request might timeout when there is large amount of data to be processed. 
<br>Increasing the collection throughput would help mitigate this issue. You can also evaluate if the queries can be optimized further by making effective use of the index.
<br>If you are wanting to delete large amounts of data without impacting RU:
* Consider using TTL (Based on Timestamp) [Expire data with Azure Cosmos DB's API for MongoDB](https://docs.microsoft.com/azure/cosmos-db/mongodb-time-to-live)
* Use Cursor/Batchsize to perform the delete. You can fetch a single document at a time and delete it through a loop. This would help you to slowly delete without impacting your production application

### **MongoDB wire version issues**
The older versions of MongoDB drivers are unable to detect the Azure Cosmos account's name in the connection strings.
<br>To correct, append *appName=@accountName@* at the end of your Cosmos DB's API for MongoDB connection string, where accountName is your Cosmos DB account name.  

### **ExceededMemoryLimit**
As a multi-tenant service, the operation has gone over the client's memory allotment.
<br>Reduce the scope of the operation through more restrictive query criteria or contact support from the Azure portal. 
<br>Example: *db.getCollection('users').aggregate([{$match: {name: "Andy"}}, {$sort: {age: -1}}]))*  



## **Recommended Documents**  

[Connect a MongoDB application to Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/connect-mongodb-account)
<br>Learn how to connect your MongoDB app to an Azure Cosmos DB by using a MongoDB connection string. You can then use an Azure Cosmos database as the data store for your MongoDB app.
<br>This tutorial provides two ways to retrieve connection string information:
* The quickstart method, for use with .NET, Node.js, MongoDB Shell, Java, and Python drivers
* The custom connection string method, for use with other drivers  

[Use Robo 3T with Azure Cosmos DB's API for MongoDB](https://docs.microsoft.com/azure/cosmos-db/mongodb-robomongo)
<br>This article will help you to add your Cosmos account to the Robo 3T connection manager.



