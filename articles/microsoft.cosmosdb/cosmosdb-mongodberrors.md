<properties
	pageTitle="MongoDB Errors"
	description="MongoDB Errors"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636778,32636789"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-mongodberrors"
	displayOrder="223"
	category="MongoDB"
	ownershipId="AzureData_AzureCosmosDB"
/>

# MongoDB - Commonly faced errors

## Common errors and solutions

| Code       | Error                | Description  | Solution  |
|------------|----------------------|--------------|-----------|
| 2 | BadValue | One common cause is that an index path corresponding to the specified order-by item is excluded or the order by query does not have a corresponding composite index that it can be served from. The query requests a sort on a field that is not indexed. | Create a matching index (or composite index) for the sort query being attempted. |
| 13 | Unauthorized | The request lacks the permissions to complete. | Ensure you are using the correct keys.  |
| 26 | NamespaceNotFound | The database or collection being referenced in the query cannot be found. | Ensure your database/collection name precisely matches the name in your query.|
| 50 | ExceededTimeLimit | The request has exceeded the timeout of 60 seconds of execution. |  There can be many causes for this error. One of the causes is when the currently allocated request units capacity is not sufficient to complete the request. This can be solved by increasing the request units of that collection or database. In other cases, this error can be worked-around by splitting a large request into smaller ones. Retrying a write operation that has received this error may result in a duplicate write. <br><br>If you are trying to delete large amounts of data without impacting RUs: <br>- Consider using TTL (Based on Timestamp): [Expire data with Azure Cosmos DB's API for MongoDB](https://docs.microsoft.com/azure/cosmos-db/mongodb-time-to-live) <br>- Use Cursor/Batch size to perform the delete. You can fetch a single document at a time and delete it through a loop. This will help you slowly delete data without impacting your production application.|
| 61 | ShardKeyNotFound | The document in your request did not contain the collection's shard key (Azure Cosmos DB partition key). | Ensure the collection's shard key is being used in the request.|
| 66 | ImmutableField | The request is attempting to change an immutable field | `id` fields are immutable. Ensure that your request does not attempt to update that field or the shard key field. |
| 67 | CannotCreateIndex | The request to create an index cannot be completed. | Up to 500 single field indexes can be created in a container. Up to eight fields can be included in a compound index (compound indexes are supported in version 3.6+). |
| 115 | CommandNotSupported | The request attempted is not supported. | Additional details should be provided in the error. If this functionality is important for your deployments, let us know by creating a support ticket in the [Azure portal](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade). |
| 11000 | DuplicateKey | The shard key (Azure Cosmos DB partition key) of the document you're inserting already exists in the collection or a unique index field constraint has been violated. | Use the update() function to update an existing document. If the unique index field constraint has been violated, insert or update the document with a field value that does not exist in the shard/partition yet. Another option would be to use a field containing a combination of the id and shard key fields. |
| 16500 | TooManyRequests  | The total number of request units consumed is more than the provisioned request-unit rate for the collection and has been throttled. | Consider scaling the throughput assigned to a container or a set of containers from the Azure portal or you can retry the operation. If you enable SSR (server-side retry), Azure Cosmos DB automatically retries the requests that fail due to this error. |
| 16501 | ExceededMemoryLimit | As a multi-tenant service, the operation has gone over the client's memory allotment. This is only applicable to Azure Cosmos DB API for MongoDB version 3.2. | Reduce the scope of the operation through more restrictive query criteria or contact support from the [Azure portal](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade). Example: `db.getCollection('users').aggregate([{$match: {name: "Andy"}}, {$sort: {age: -1}}]))` |
| 40324 | Unrecognized pipeline stage name. | The stage name in your aggregation pipeline request was not recognized. | Ensure that all aggregation pipeline names are valid in your request. |
| - | MongoDB wire version issues | The older versions of MongoDB drivers are unable to detect the Azure Cosmos account's name in the connection strings. | Append `appName=@accountName@` at the end of your Cosmos DB's API for MongoDB connection string, where `accountName` is your Cosmos DB account name. |
| - | MongoDB client networking issues (such as socket or endOfStream exceptions)| The network request has failed. This is often caused by an inactive TCP connection that the MongoDB client is attempting to use. MongoDB drivers often utilize connection pooling, which results in a random connection chosen from the pool being used for a request. Inactive connections typically timeout on the Azure Cosmos DB end after four minutes. | You can either retry these failed requests in your application code, change your MongoDB client (driver) settings to teardown inactive TCP connections before the four-minute timeout window, or configure your OS `keepalive` settings to maintain the TCP connections in an active state.<br><br>To avoid connectivity messages, you may want to change the connection string to set `maxConnectionIdleTime` to 1-2 minutes.<br>- Mongo driver: configure `maxIdleTimeMS=120000` <br>- Node.JS: configure `socketTimeoutMS=120000`, `autoReconnect` = true, `keepAlive` = true, `keepAliveInitialDelay` = 3 minutes
| - | Mongo Shell not working in the Azure portal | When user is trying to open a Mongo shell, nothing happens and the tab stays blank.  | Check Firewall. Firewall is not supported with the Mongo shell in the Azure portal. <br>- Install Mongo shell on the local computer within the firewall rules <br>- Use legacy Mongo shell
| - | Unable to connect with connection string  | The connection string has changed when upgrading from 3.2 -> 3.6 | Note that when using Azure Cosmos DB's API for MongoDB accounts, the 3.6 version of accounts have the endpoint in the format `*.mongo.cosmos.azure.com` whereas the 3.2 version of accounts have the endpoint in the format `*.documents.azure.com`.  

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
