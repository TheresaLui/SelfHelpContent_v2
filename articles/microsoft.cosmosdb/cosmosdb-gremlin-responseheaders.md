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
	displayOrder="285"
	category="Gremlin (Graph)"
/>
# Gremlin - Response Headers

Gremlin engine returns a set of headers with every response that are recommended to be captured and logged by client applications:

* **x-ms-request-charge**: Throughput cost of gremlin traversal in RU/s for a given partial message
* **x-ms-total-request-charge**: Cumulative throughput cost of gremlin traversal in RU/s of all partial messages up to that point. When combined throughput of all traversals per second exceeds provisioned collection or database throughput, traversals are throttled.
* **x-ms-status-code**: This is an HTTP status code that classifies response to the client
* **x-ms-retry-after-ms**: A value in timespan format (00:00:02.5000000) after which throttled request can be retried. Traversal that is retried before specified time elapses will likely be throttled again.
* **x-ms-activity-id**: Unique identifier of a traversal activity on the server side. When there is a problem with traversal, it is very useful to share this identifier with support team.

These attributes can be retrieved from the client driver:

* **Gremlin.Net**

```
GremlinServer gremlinServer = new GremlinServer(...);
GremlinClient gremlinClient = new GremlinClient(gremlinServer, ...);

ResultSet<dynamic> resultSet = gremlinClient.SubmitAsync<dynamic>(...);

// This line reads the response status code
Console.WriteLine($"[\"x-ms-status-code\"] = { resultSet.StatusAttributes["x-ms-status-code"] }");
```

* **TinkerPop Java Gremlin Client**

```
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

Common status code values customers see are listed below:

* **404**: Concurrent operations that attempts to delete and update the same edge or vertex simultaneously. Error message `"Owner resource does not exist"` indicates that specified database or collection is incorrect in connection parameters in `/dbs/<database name>/colls/<collection or graph name>` format.
* **409**: `Conflicting request to resource has been attempted. Retry to avoid conflicts.` This usually happens when vertex or an edge with an identifier already exists in the graph.
* **412**: Status code is usually complemented with error message `"PreconditionFailedException": One of the specified pre-condition is not met`. This is indicative of an optimistic concurrency control violation between reading an edge or vertex and writing it back to the store after modification. Most common situations when this occurs is property modification, for example `g.V('identifier').property('name','value')`. Gremlin engine would read the vertex, perform modification and write it back. If two traversals concurrently read and write the same vertex or an edge one of them will receive this error. It is recommended to retry traversal again.
* **429**: Request was throttled and should be retried after value in **x-ms-retry-after-ms**
* **500**: Error message that contains `"NotFoundException: Entity with the specified id does not exist in the system."` indicates that a database and/or collection was re-created with the same name. This error will disappear within 5 minutes as change propagates and invalidates caches in different Cosmos DB components. To avoid this issue, use unique database and collection names every time.

## **Recommended Documents**

* [TinkerPop Status Codes](http://tinkerpop.apache.org/docs/3.0.2-SNAPSHOT/#_developing_a_driver)
* [How to find Request Unit charge](https://docs.microsoft.com/azure/cosmos-db/find-request-unit-charge#gremlin-api)
