<properties
	pageTitle="MongoDB.Driver.MongoWaitQueueFullException issue"
	description="MongoDB.Driver.MongoWaitQueueFullException issue"
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
	articleId="c7c57003-3b60-44f7-80f0-04c2b1c915f7"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# MongoDB.Driver.MongoWaitQueueFullException issue

<!--issueDescription-->

Customer is trying to connect their service and is having difficulties connecting to CosmosDB therefore the health check would fail frequently.

Looks like this is a known issue mongo driver. Here is one of the solution suggested by the mongo community https://jira.mongodb.org/browse/CSHARP-1180 

Provide customer with ready message below.

### Customer Message
Dear customer,

This exception is not necessarily a bug. It just indicates that too many threads are trying to use MongoDB at once. In the example provided in the description the code is trying to do 100,000 inserts in parallel. By default the connection pool has 100 connections. Threads pull connections from the connection pool and return them when they are done. Once all connections are in use, any further threads that want a connection must wait for some other thread to return a connection to the pool. The driver limits the number of threads that are allowed to wait for a connection at the same time. The default limit is 500. With 100,000 parallel inserts it's not unexpected that more than 600 threads might be actively trying to do an insert at the same time, which will result in this exception being thrown. The solution is to either decrease the number of threads trying to use MongoDB at the same time (decrease the degree of parallelism) or to configure the connection pool to have either more connections or a higher wait queue limit, or both. If you see this exception and you know there are fewer than 600 threads that would be something we would like to reproduce.

Please kindly also find below one of the solution suggested by the mongo community:

https://jira.mongodb.org/browse/CSHARP-1180 

Thank you.

<!--/issueDescription-->

