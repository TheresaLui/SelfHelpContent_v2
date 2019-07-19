<properties
	pageTitle="MongoDB Errors"
	description="MongoDB Errors"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	ms.author="bharathb"
	selfHelpType="resource"
	supportTopicIds="32636778,32636789,32636810"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-mongodberrors"
	displayOrder="223"
	category="MongoDB"
/>
# MongoDB - Commonly faced errors

## **Recommended Steps**

### **Client connection errors**
Mongo client drivers use “connection pooling”. Whenever a mongo client is initialized to a remote address, the driver establishes more than one connection. On the server side, connections which are idle for more than 30 minutes are automatically closed down.
It is possible that some of the connections in the connection pool would timeout (if that connection was not picked by driver to issue user commands for sometime).
To avoid connectivity messages, change the connection string to set maxConnectionIdleTime to 1-2 minutes.

### **Request rate exceeded errors**
Some of the queries including aggregations require a large amount of processing. If the collection's throughput is not enough, you will see these errors. You can confirm this by going to the Metrics blade and selecting the Throughput tab for your collection. 
You can also evaluate if the queries can be optimized further by making effective use of the index

### **Request timeout errors**
While executing a query using the Mongo API for CosmosDB, the request might timeout when there is large amount of data to be processed. Increasing the collection throughput would help mitigate this issue.You can also evaluate if the queries can be optimized further by making effective use of the index.

