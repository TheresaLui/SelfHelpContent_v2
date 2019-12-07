<properties
	pageTitle="Gremlin Getting Started"
	description="Article describes how to get started with Gremlin after account provisioning"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="olignat"
	ms.author="olignat"
	selfHelpType="generic"
	supportTopicIds="32675632"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-gremlin-getstarted"
	displayOrder="180"
	category="Gremlin (Graph)"
/>

# Getting Started with Gremlin

Gremlin is a graph traversal language of [Apache TinkerPop](http://tinkerpop.apache.org/) and it is rapidly becoming the industry standard for accessing data in graph databases.

## **Recommended Steps**

To try Gremlin for the first time or explore graph traversals, it is recommended that you use Data Explorer from Azure Portal. Gremlin can be accessed from the Data Explorer tab on the Azure Cosmos DB account resource page. Create a new graph, and use a query text box on the web page to insert vertices and edges as well as traverse them. Refer to [Graph Traversal Steps](https://tinkerpop.apache.org/docs/current/reference/#graph-traversal-steps) to learn about available operations and how to use them.

1. Retrieve 10 vertices: `g.V().limit(10)`
2. Retrieve 10 edges: `g.E().limit(10)`
3. Create a vertex with properties: `g.addV('business').property('id', 'city-1').property('name','Seattle')`
4. Create an edge between two existing vertices: `g.V('city-1').addE('is-driving-distance-from').to(g.V('city-2'))`
5. Find all cities in driving distance from places of business: `g.V().hasLabel('business').outE('is-driving-distance-from').inV()`

### Use Gremlin from an App

To access Gremlin account from an application please use one of the recommended clients:

1. [Gremlin.Net](https://www.nuget.org/packages/Gremlin.Net) for .NET applications:

```
using (GremlinServer server = new GremlinServer("<account fully qualified domain name>", 443, true, $"/dbs/{<database name/colls/{<graph or collection name>}", $"{<account key>}"))
using (GremlinClient client = new GremlinClient(server, new GraphSON2Reader(), new GraphSON2Writer(), GremlinClient.GraphSON2MimeType))
{
    IEnumerable<object> result = await client.SubmitAsync<object>(requestScript: "g.V().limit(10)");
}
```

2. [TinkerPop Gremlin Java Client](https://mvnrepository.com/artifact/com.tinkerpop.gremlin/gremlin-java):

```
Cluster.Builder builder = Cluster.build();
builder.addContactPoint(<account fully qualified domain name>);
builder.port(443);

AuthProperties authenticationProperties = new AuthProperties();
authenticationProperties.with(AuthProperties.Property.USERNAME, String.format("/dbs/%s/colls/%s", <database name>, <graph or collection name>));
authenticationProperties.with(AuthProperties.Property.PASSWORD, this.key);

builder.authProperties(authenticationProperties);
builder.enableSsl(true);

Map<String, Object> config = new HashMap<String, Object>();
config.put("serializeResultToString", "true");

GraphSONMessageSerializerV1d0 serializer = new GraphSONMessageSerializerV1d0();
serializer.configure(config, null);

builder.serializer(serializer);

Cluster cluster = builder.create();
Client client = cluster.connect();

ResultSet resultSet = client.submit("g.V().limit(10)");
List<Result> results = resultSet.all().get();
```

3. [Node.js](https://www.npmjs.com/package/gremlin):

```
'use strict';
var gremlin = require("gremlin");

var client = gremlin.createClient(
    443,
    "<account fully qualified domain name>", {
        "session": false,
        "ssl": true,
        "user": `/dbs/${<database name>}/colls/${<collection or graph name>}`,
        "password": "<account key>"
    }

client.execute("g.V().drop()", {}, (err, results) => {
		if (err) {
		}
    });
);
```

4. [Python](https://pypi.org/project/gremlinpython/):

```
from gremlin_python.driver import client, serializer

	client = client.Client('wss://<fully qualified account name>:443/', 'g',
		username='/dbs/<database name>/colls/<graph or collection name>',
		password='<account key>', 
		message_serializer=serializer.GraphSONSerializersV2d0()

    callback = client.submitAsync("g.V().count()")
    for result in callback.result():
        print('Node count {}'.format(result[0]))
```

5. [PHP](https://packagist.org/packages/brightzone/gremlin-php)

## **Recommended Documents**

* [Import data into Cosmos DB Gremlin account](https://docs.microsoft.com/azure/cosmos-db/bulk-executor-graph-dotnet)
* [Development using the Gremlin API](https://docs.microsoft.com/azure/cosmos-db/graph-introduction#get-started)
* [Supported Gremlin operators](https://docs.microsoft.com/azure/cosmos-db/gremlin-support)
* [Graph data partitioning](https://docs.microsoft.com/azure/cosmos-db/graph-partitioning)
