<properties
	  pageTitle="Use composite Index to reduce the High RU cost"
	  description="Use composite Index to reduce the High RU cost"
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
	  articleId="57761c40-08ae-4d8e-a8a3-e54edca101ac"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Use composite Index to reduce the High RU cost

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** Investigate by looking at the content below.

#### When does Composite Index Required
Composite index is required for a SQL Query which have an ORDER BY with two or more properties

#### What are the various  Query Patterns with Composite Index would help? 

| **Composite Index**                 | **Sample ORDER BY Query**                                    | **Supported by Composite Index?** | **Explanation**                                              |
| ----------------------------------- | ------------------------------------------------------------ | --------------------------------- | ------------------------------------------------------------ |
| (name ASC, age  ASC)                | SELECT * FROM c  ORDER BY c.name ASC, c.age asc              | Yes                               | The query has  order by matches with the composite index properties and ascending clause |
| (name ASC, age  ASC)                | SELECT * FROM c  ORDER BY c.name DESC, c.age DESC            | Yes                               | If the query?s  ORDER BY clause?s order is the opposite of a composite index for all  properties, then it can utilize  the composite index. |
| (name ASC, age  ASC, timestamp ASC) | SELECT * FROM c  ORDER BY c.name ASC, c.age ASC, timestamp ASC | Yes                               | The Query has  order by property which matches composite index sequence and order |
| (name  ASC, age ASC).               | SELECT * FROM c WHERE c.name = "John" AND c.age = 18         | Yes                               | The query has  equality filters on properties that are included in the composite index. The  composite index will be used but likely won?t have huge RU charge improvement  over using range indexes (but will still be an improvement). In this case,  the ORDER (ASC or DESC) does not matter. |
| (name  ASC, age ASC).               | SELECT * FROM c WHERE c.name = "John" AND c.age > 18         | Yes                               | The query has  equality filters and a maximum of one range filter (!=, >, <, <=, or  >=) so it will use the corresponding composite index that is created on  name and age. In this case, the ORDER (ASC or DESC) does not matter. |
| (name DESC, age  ASC)               | SELECT * FROM c  WHERE c.name = "John" AND c.age > 18        | Yes                               | Same as above.  In this case, the ORDER (ASC or DESC) does not matter. |
| (name ASC, age  ASC, timestamp ASC) | SELECT * FROM c  WHERE c.name = "John" AND c.age = 18 AND c.timestamp > 123049923 | Yes                               | Same as above.  In this case we added on additional equality filters but as long as we  have a maximum of one range filter (!=, >, <, <=, or >=)   this query will still fully utilize the composite index. |
| (name ASC, timestamp ASC)           | SELECT * FROM c WHERE c.name =  "John" ORDER BY c.name ASC, c.timestamp ASC | Yes                               | This query will  utilize the composite index because the ORDER BY clause has properties which  have the same sequence and order value as the properties in the composite  index. |

 
#### What are the various  Query Patterns in which the Composite Index would NOT help?

| (name ASC, age ASC)                   | SELECT * FROM c  ORDER BY c.age ASC, c.name asc              | No   | The Query has  order by property which is not matching in the composite index i.e. age  property |
| ------------------------------------- | ------------------------------------------------------------ | ---- | ------------------------------------------------------------ |
| (name ASC, age  ASC)                  | SELECT * FROM c  ORDER BY c.name ASC, c.age DESC             | No   | The order value  should match (or be opposite for all properties) |
| (name ASC, age  ASC, timestamp ASC)   | SELECT * FROM c  ORDER BY c.name ASC, c.age ASC              | No   | The Query has  order by property which is not matching in the composite index (there is an  extra property) |
| (name ASC, age  ASC)                  | SELECT * FROM c  WHERE c.name != "John" AND c.age > 18       | No   | There can only  be a maximum of one range filter (!=, >, <, <=, or >=)  for  a query to utilize a composite index for filters on those properties |
| (name ASC,  timestamp ASC)            | SELECT * FROM c  WHERE c.name = "John" ORDER BY c.timestamp ASC | No   | The name  is not included in the order clause                |
| `(name ASC, timestamp ASC)`           | SELECT * FROM c  WHERE c.name = "John" ORDER BY c.timestamp ASC, c.name ASC | No   | The  order by clause is not in the same sequence of the composite index |
| (age ASC, name  ASC, timestamp ASC) | SELECT * FROM c  WHERE c.age = 18 and c.name = "John" ORDER BY c.timestamp ASC | No   | The age and  name are not included in the ORDER BY clause    |
| (name ASC, age  ASC, timestamp ASC)   | SELECT * FROM c  WHERE c.name = "John" AND c.age < 18 AND c.timestamp = 123049923 | No   | If a query has  filters that will utilize a composite index, the inequality filter must be on  the last property defined in the composite index |


#### How to review telemetry to check the Composite Index might help to reduce the cost of the Query?

 
```
let databaseaccount="cjc6nd6ms8hxomswtxkrkjjrm39zs";
let collectionRid = "Dc4DAOiufAA=";
SqlQueryExecMetrics    
| where TIMESTAMP >= ago(1d) 
| where databaseaccount contains databaseaccount
| where CollectionId  == collectionRid 
| where IndexVersion  ==1
| where Shape contains "OrderBy"   
| where ScalarExprCount <= 8
| where ExcludedTermCount > 500 or IncludedTermCount  > 500
| where QueryCharge > 50
```

#### Does adding the composite index trigger index full rebuild ? 
No. 

#### How does the index get built when composite is added to the existing index.
The additional composite index is build without impacting the existing index. However, the newly building index would not be used by the query optimization until the composite index is fully built.

#### Does the composite index build have any impact on provisioned RUs? 
The build does consume the provisioned RU.  Increasing the Provisioned RU would help build faster or adding the composite index when less usage is recommended.

#### Query is still failing ever after composite index is created 
 The Key thing to emphasize is that if a customer has the following query:

 SELECT * FROM c ORDER BY a,b 

If they try to run this when the composite index addition is not complete, they will get an error telling them to add a composite index (even if they had just added one). As of now, the error message doesn?t mention that they have an index rebuild in progress that will eventually allow the query. 

## Customer message: 
Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query.

<!--/issueDescription-->

