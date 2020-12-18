<properties
	  pageTitle="Connection Issue Error: MongoDB.Driver.MongoConnectionException"
	  description="Connection Issue Error: MongoDB.Driver.MongoConnectionException"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="ceb4c3f0-0636-4c4c-a79c-db157c318408"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Connection Issue Error: MongoDB.Driver.MongoConnectionException

<!--issueDescription-->

Dear customer,

Inactive TCP connections starting after 4 minutes are torn down by the Azure Load Balancer.  Mongo drivers are unaware of when connections are torn down by the server and reuse these torn down connections causing socket/connection exceptions.  
Mongo Clients can handle this in two ways:
* Retry/reconnect on connection/socket exceptions
* Configure the client to tear down TCP connections before Cosmos DB does

**Info:** Mongo drivers support connection pooling which mean n connection are used to submit requests.  The driver randomly uses the connection from the pool, so if the client application is not active enough or idle then some connections from the pool can be idle for too long.
 
**Driver settings:**  Configure maxIdleTimeMS < 3 minutes
The goal here is to make the drivers tear down the TCP connection before Cosmos DB so the client can do a graceful closure and reconnect.  
This will cause the driver to close connections that have been idle and are at risk of being torn down by Cosmos DB. [Connection String URI Format](https://docs.mongodb.com/manual/reference/connection-string/)  

**NodeJS driver:** Configure socketTimeoutMS < 3 minutes, autoReconnect = true, keepAlive = true, keepAliveInitialDelay = 3 minutes  
In NodeJS this setting operates similar to maxIdleTimeMS. [Connection Options](https://mongoosejs.com/docs/connections.html#options),[MongoClient.connect](http://mongodb.github.io/node-mongodb-native/3.1/api/MongoClient.html#.connect)  

**OS settings:**  
The goal is for the operating system to maintain TCP connections such that they will not be torn down.  
Configure the OS TCP keepalive to use the following values
 
**You will need to configure both values.**
* TCP KeepAlive Time = 3 minutes
* TCP KeepAlive Interval = 60 seconds

Thank you.

<!--/issueDescription-->

