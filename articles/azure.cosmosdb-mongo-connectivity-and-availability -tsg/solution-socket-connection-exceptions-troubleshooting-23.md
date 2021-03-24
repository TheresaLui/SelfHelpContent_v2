<properties
	  pageTitle="Socket Connection Exceptions troubleshooting"
	  description="Socket Connection Exceptions troubleshooting"
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
	  articleId="c992e3f2-af67-4cdc-b4e9-00d479d03291"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Socket Connection Exceptions troubleshooting

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

#### Follow all steps below before opening an incident with PG
If all of the below steps fail, collect all connection details from the **details shared below** plus details shared in **9. Connection Debug TSG**, and then transfer the CRI to MongoDB PG for further investigation.?


## Customer message:
Dear customer,

Inactive TCP connections starting after 4 minutes are torn down by the Azure Load Balancer.  Mongo drivers are unaware of when connections are torn down by the server and reuse torn down connections causing socket/connection exceptions. Clients can handle this in two ways:

1) Retry/reconnect on connection/socket exceptions
2) Configure the client to tear down TCP connections before Cosmos DB does
 
Info: Mongo drivers support connection pooling which mean n connection are used to submit requests.  The driver randomly uses the connection from the pool, so if the client application is not active enough or idle then some connections from the pool can be idle for too long. A scenario that frequently sees this occur is when the customers application makes less requests.

Sample error from mongo shell:
<pre>
globaldb:PRIMARY> db.test2.count()
2020-09-17T18:28:15.750+0530 I NETWORK  [thread1] Socket  send() An existing connection was forcibly closed by the remote host. 52.179.143.233:10255
2020-09-17T18:28:15.751+0530 E QUERY    [thread1] Error: socket exception [SEND_ERROR] for 52.179.143.233:10255 :
runClientFunctionWithRetries@src/mongo/shell/session.js:329:27
runCommand@src/mongo/shell/session.js:423:25
DB.prototype._runCommandImpl@src/mongo/shell/db.js:145:16
DB.prototype.runCommand@src/mongo/shell/db.js:161:20
DB.prototype.runReadCommand@src/mongo/shell/db.js:139:16
DBQuery.prototype.count@src/mongo/shell/query.js:388:15
DBCollection.prototype.count@src/mongo/shell/collection.js:1596:12
@(shell):1:1
2020-09-17T18:28:15.751+0530 I NETWORK  [thread1] Marking host cdb-ms-prod-eastus2-cm1.documents.azure.com:10255 as failed :: caused by :: Location40657: Last known master host cannot be reached
globaldb:PRIMARY> db.test2.count()
1548856
globaldb:PRIMARY>
</pre>

**Note:** You will only need to implement one of the options below

<br>

#### FAQ:
But my application has been working for X amount of time without an issue: although the client application code has not changed there can be changes in request volume and load, networking condition, etc that can lead to this issue. Handling this scenario is good practice because there is always a chance of getting this exceptions when working over a network.

#### Option 1: Client Code Handling
MongoDB drivers do not handle retries well so this logic will need to be written in the client code.

#### Option 2: Driver Settings
The goal is to make the drivers tear down the TCP connection before Cosmos DB so the client can do a graceful closure and reconnect.

For all drivers (and mongo shell) except nodejs: <br/>
Configure maxIdleTimeMS < 3 minutes
- This will cause the driver to close connections that have been idle and are at risk of being torn down by Cosmos DB
- Note that this does not work in all drivers (NodeJS)
- https://docs.mongodb.com/manual/reference/connection-string/  

NodeJS driver: <br/>
Configure socketTimeoutMS < 3 minutes, autoReconnect = true, keepAlive = true, keepAliveInitialDelay = 3 minutes
- In NodeJS this setting operates similar to maxIdleTimeMS. NodeJS does not accept maxIdleTime. So, use the connection string from portal and options above as the connection parameters.
- https://mongoosejs.com/docs/connections.html#options, http://mongodb.github.io/node-mongodb-native/3.1/api/MongoClient.html#.connect

#### Option 3: Operating System Settings
The goal is for the operating system to maintain TCP connections such that they will not be torn down.

Configure the OS TCP keepalive to use the following values
 
- The customer will need to configure both values
- TCP KeepAlive Time = 3 minutes
- TCP KeepAlive Interval = 60 seconds

Windows: https://blogs.technet.microsoft.com/nettracer/2010/06/03/things-that-you-may-want-to-know-about-tcp-keepalives/  
Linux: http://www.tldp.org/HOWTO/TCP-Keepalive-HOWTO/usingkeepalive.html  
Mac: http://coryklein.com/tcp/2015/11/25/custom-configuration-of-tcp-socket-keep-alive-timeouts.html  
Mongo Docs: https://docs.mongodb.com/manual/faq/diagnostics/#does-tcp-keepalive-time-affect-mongodb-deployments  

Thank you.

<!--/issueDescription-->

