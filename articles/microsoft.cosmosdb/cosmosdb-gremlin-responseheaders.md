<properties
	pageTitle="Gremlin response headers"
	description="Metadata headers returned by Gremlin query engine"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="olignat"
	ms.author="olignat"
	selfHelpType="generic"
	supportTopicIds="32675636"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-gremlin-responseheaders"
/>
# Gremlin - Response Headers

Gremlin engine returns a set of headers with every response that are recommended to be captured and logged by client applications. 

**Header** | **Explanation**
--- | ---
***x-ms-request-charge***  | Total throughput cost of gremlin traversal in RU/s. When compbined throughput of all traversals per second exceeds provisioned collection or database throughput, traversals are throttled.
***x-ms-status-code*** | This is an HTTP status code that classifies response to the client.
***x-ms-retry-after-ms*** | A value in timespan format (00:00:02.5000000) after which throttled request can be retried. Traversal that is retried before specified time elapses will likely be throttled again.
***x-ms-activity-id*** | Unique identifier of a traversal activity on the server side. When there is a problem with traversal, it is very useful to share this identifier with support team.

These attributes can be retrieved from the client drvier.
* ***Gremlin.Net***
```C#
GremlinServer gremlinServer = new GremlinServer(...);
GremlinClient gremlinClient = new GremlinClient(gremlinServer, ...);

ResultSet<dynamic> resultSet = gremlinClient.SubmitAsync<dynamic>(...);

// This line reads the response status code
Console.WriteLine($"[\"x-ms-status-code\"] = { resultSet.StatusAttributes["x-ms-status-code"] }");
```

* ***TinkerPop Java Gremlin Client***
```Java
Cluster cluster = builder.create();
Client client = cluster.connect();

try {
    client.submit(...));
}
catch (ResponseException e) {
    // Read status code here
    Object statusCode = re.getStatusAttributes().getOrDefault("x-ms-status-code", null);
}
```

Common status code values customers see are listed below

**Status Code** | **Explanation**
--- | ---
***404*** | Concurrent operations that attempts to delete and update the same edge or vertex simultaneously. Error message `"Owner resource does not exist"` indicates that specified database or collection is incorrect in connection parameters in `/dbs/<database name>/colls/<collection or graph name>` format.
***409*** | Request encountered a conflicting write operation. This usually happens when vertex or an edge with an identifier already exists in the graph.
***429***  | Request was throttled and should be retried after value in ***x-ms-retry-after-ms***.

## **Recommended Documents**
* [TinkerPop Status Codes](http://tinkerpop.apache.org/docs/3.0.2-SNAPSHOT/#_developing_a_driver)
