<properties
	pageTitle="Gremlin unsupported features"
	description="High-level scope of what is explicitly unsupported in Gremlin"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="olignat"
	ms.author="olignat"
	selfHelpType="resource"
	supportTopicIds="32675638,32684531"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-gremlin-unsupported"
	displayOrder="187"
	category="Gremlin (Graph)"
/>
# Gremlin - Unsupported Features

Gremlin follows very closely [Apache TinkerPop](https://tinkerpop.apache.org/docs/current/reference/#graph-traversal-steps) traversal steps specification but a few things are not yet available:

* ***[Gremlin Bytecode](http://tinkerpop.apache.org/docs/current/tutorials/gremlin-language-variants/)*** is a programming language agnostic specification for graph traversals. Cosmos DB does not yet support it. Please use ```GremlinClient.SubmitAsync()``` and pass traversal as a text string. Support for Bytecode should be available in near future.

* ***```property(set, 'xyz', 1)```*** set cardinality is not supported today. Support for set property cardinality will be enabled in the future. Please use ```property(list, 'xyz', 1)``` today.

* ***Objects as properties*** on vertices or edges are not supported. Properties can only be primitive types or arrays.

* ***Sorting by array properties*** ```.order().by(<array property>)``` is not supported. Sorting is supported only by primitive types.

* ***Non-primitive JSON types*** are not supported. Please use ```string```, ```number``` or ```true```/```false``` types. ```null``` values are not supported. 

* ***GraphSONv3*** serializer is not available today but will become available in near future.

* ***Transactions*** are not supported due to distributed nature of the system. Please configure desired consistency model on Gremlin account to "read your own writes".

## **Recommended Documents**

Please share your feedback on features you'd like to see in Cosmos DB Gremlin engine on page. Perhaps your feature has already been requested by a customer or a community member.

* [Cosmos DB User Voice](https://feedback.azure.com/forums/263030-azure-cosmos-db) 
