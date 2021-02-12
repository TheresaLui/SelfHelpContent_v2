<properties
    pageTitle="MongoDB Connection Errors RCA"
    description="RCA - MongoDB Connection Errors"
    infoBubbleText="MongoDB connections to your account were closed due to timeouts. See the details on the right."
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="bharathsreenivas"
    ms.author="bharathb"
    articleId="cosmosdb-mongoconnection-rca"
    diagnosticScenario="CosmosDBMongoInsight"
    selfHelpType="rca"
    supportTopicIds="32636757"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# MongoDB Connection Errors

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Some of the MongoDB connections to your account were closed due to timeouts.
<!--/issueDescription-->

MongoDB client drivers use connection pooling. Whenever a MongoDB client is initialized to a remote address, the driver establishes more than one connection.
One of the connections is used to send regular periodic commands like isMaster and ping.
The other connections are used to issue user commands like query, insert and delete.
If a connection in the connection pool is not used by a driver to issue user commands, the connection will timeout based on the configured timeout limit. Once a connection times out, it is removed from the pool.
Because CosmosDB is a multi tenant service, we tear down TCP connections which are not used within the default timeout period.

## **Recommended Steps**

To avoid connectivity problems, increase the value of maxConnectionIdleTime property and other properties listed in the nodejs example below

```
MongoClientOptions.Builder optionsBuilder = new MongoClientOptions.Builder();
optionsBuilder.socketTimeout(10000);
optionsBuilder.maxConnectionIdleTime(60000);
optionsBuilder.heartbeatConnectTimeout(5000);
MongoClientURI mongoClientURI = new MongoClientURI(props.getMongoDbConnection(), optionsBuilder);
```
