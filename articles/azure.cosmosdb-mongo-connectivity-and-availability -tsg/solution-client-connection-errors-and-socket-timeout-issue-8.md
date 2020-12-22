<properties
	  pageTitle="Client connection errors and socket timeout issue"
	  description="Client connection errors and socket timeout issue"
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
	  articleId="209526da-77c6-47aa-924f-837e4d33cb7c"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Client connection errors and socket timeout issue

<!--issueDescription-->

Dear customer,

Mongo client drivers use "connection pooling". Whenever a mongo client is initialized to a remote address, the driver establishes more than one connection. On the server side, Inactive/Idle TCP connections which are idle for more than 30 minutes are automatically closed by the Azure Cosmos DB Mongo server.  
Mongo drivers are unaware of when connections are torn down by the server and reuse of torn down connections by new requests causes socket/connection exceptions.  
Retry/reconnect on connection/socket exceptions.  

To avoid connectivity messages, you may want to change the connection string to set maxConnectionIdleTime to 1-2 minutes.
* Mongo driver: configure *maxIdleTimeMS=120000* 
* Node.JS: configure *socketTimeoutMS=120000*, *autoReconnect* = true, *keepAlive* = true, *keepAliveInitialDelay* = 3 minutes

Tear down TCP connections at the client.
* Configure the client to tear down TCP connections before Cosmos DB does 

Thank you.

<!--/issueDescription-->

