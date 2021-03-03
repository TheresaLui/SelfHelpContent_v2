<properties
	  pageTitle="MongoSocketWriteException Errors issue"
	  description="MongoSocketWriteException Errors issue"
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
	  articleId="b755580b-de5f-4ba7-9f62-4787a0bd3628"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# MongoSocketWriteException Errors issue

<!--issueDescription-->
Dear customer,

Your connection fails or is closed with one of the following error stacks:
**java.lang.Exception: Exception sending message; nested exception is *com.mongodb.MongoSocketWriteException: Exception sending message***

### Cause
- Cosmos DB Server is configured with idle to timeout after 30 minutes of idleness.  This means any connection which have not submitted any request for 30 minutes would be killed by the Server.
- The Client does not know that the server have killed the connection and the driver is reusing the connection for the request generating the above exception.

### Connection Pool Behavior
- The Mongo driver supports connection pool which mean n connection is used to submit the request.   The driver randomly uses the connection from the pool. So if the client application is not active enough or idle then some connection from the pool is idle for more than 30 minutes which is not known by the driver. The driver reuses the connection to submit the request and generate the exception.
- The Parameter "maxIdleTimeMS" can be part of connection string which help the driver to close the connection and reopen when required.
 
#### maxIdleTimeMS
The maximum number of milliseconds that a connection can remain idle in the pool before being removed and closed.  
This option is not supported by all drivers.

The "maxIdleTimeMS" is supported by the following languages and drivers.

- Pymongo - https://api.mongodb.com/python/current/api/pymongo/mongo_client.html#pymongo.mongo_client.MongoClient.max_idle_time_ms
- c# - https://api.mongodb.com/csharp/2.0/html/P_MongoDB_Driver_MongoClientSettings_MaxConnectionIdleTime.htm
- Node.js - https://docs.mongodb.com/manual/reference/connection-string/
- Mongoose -https://docs.mongodb.com/manual/reference/connection-string/
- Springboot. -  This https://github.com/spring-projects/spring-data-mongodb) build on the official mongo driver so the connections should be managed the same way so this setting should be passed through the connection string as well.
 
### Resolution / Mitigation
Ensure the customer is using the "maxIdleTimeMS" in the connection string.

Thank you.



<!--/issueDescription-->

