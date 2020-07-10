<properties
	pageTitle="Gremlin unsupported features"
	description="High-level scope of what is explicitly unsupported in Gremlin"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32675638"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-gremlin-unsupported"
	displayOrder="187"
	category="Gremlin (Graph)"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Gremlin - Unsupported Features

Most users are able to resolve their Gremlin data issue using the steps below. 


## **Recommended Steps**  


### **Commands**
Gremlin follows very closely [Apache TinkerPop](https://tinkerpop.apache.org/docs/current/reference/#graph-traversal-steps) traversal steps specification but a few things are not yet available:

* ***[Gremlin Bytecode](http://tinkerpop.apache.org/docs/current/tutorials/gremlin-language-variants/)*** is a programming language agnostic specification for graph traversals. Cosmos DB does not yet support it. Please use ```GremlinClient.SubmitAsync()``` and pass traversal as a text string. Support for Bytecode should be available in near future.

* ***```property(set, 'xyz', 1)```*** set cardinality is not supported today. Support for set property cardinality will be enabled in the future. Please use ```property(list, 'xyz', 1)``` today.

* ***Objects as properties*** on vertices or edges are not supported. Properties can only be primitive types or arrays.

* ***Sorting by array properties*** ```.order().by(<array property>)``` is not supported. Sorting is supported only by primitive types.

* ***Non-primitive JSON types*** are not supported. Please use ```string```, ```number``` or ```true```/```false``` types. ```null``` values are not supported. 

* ***GraphSONv3*** serializer is not available today but will become available in near future.

* ***Transactions*** are not supported due to distributed nature of the system. Please configure desired consistency model on Gremlin account to "read your own writes".


### **Case-insensitive string functions with Gremlin API**
As of now this case insensitive search feature in Gremlin is not supported .  The official Tinkerpop Gremlin spec itself does not have a way to specify case insensitivity in the predicate.  
You can search with Text containing string filtering function using the SQL query for the gremlin account.  
**Example:** SQL query to filter on DisplayName property of a vertex

```
SELECT c.DisplayName FROM c WHERE CONTAINS(c.DisplayName[0]._value, "ab5", true)
```   




## **Recommended Documents**

Please share your feedback on features you'd like to see in Cosmos DB Gremlin engine on page. Perhaps your feature has already been requested by a customer or a community member.

* [Cosmos DB User Voice](https://feedback.azure.com/forums/263030-azure-cosmos-db) 
