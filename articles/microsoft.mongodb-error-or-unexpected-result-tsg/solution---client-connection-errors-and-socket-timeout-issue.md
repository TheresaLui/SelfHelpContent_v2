<properties
	pageTitle="Client connection errors and socket timeout issue"
	description="Client connection errors and socket timeout issue"
	service="Microsoft.DocumentDB"
	resource="databaseAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a93d9981-dda8-42fc-8d21-fc51bca11d93"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Client connection errors and socket timeout issue

<!--issueDescription-->

Dear customer,

Regarding client connection errors and socket timeout, Mongo client drivers use "connection pooling". Whenever a mongo client is initialized to a remote address, the driver establishes more than one connection. On the server side, Inactive/Idle TCP connections which are idle for more than 30 minutes are automatically closed by the Azure Cosmos DB Mongo server.
Mongo drivers are unaware of when connections are torn down by the server and reuse of torn down connections by new requests causes socket/connection exceptions.
Retry/reconnect on connection/socket exceptions.

To avoid connectivity messages, you may want to change the connection string to set maxConnectionIdleTime to 1-2 minutes.

1. Mongo driver: configure maxIdleTimeMS=120000
2. Node.JS: configure socketTimeoutMS=120000, autoReconnect = true, keepAlive = true, keepAliveInitialDelay = 3 minutes as per https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-tcp-idle-timeout Also, please set keepAlive: true.

Thank you.

<!--/issueDescription-->

