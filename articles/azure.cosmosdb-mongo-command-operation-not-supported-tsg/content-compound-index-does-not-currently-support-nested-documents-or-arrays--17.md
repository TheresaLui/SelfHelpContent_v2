<properties
	  pageTitle="Compound index does not currently support nested documents or arrays "
	  description="Compound index does not currently support nested documents or arrays "
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
	  articleId="651afcc2-8fea-4cdf-9fb6-b66b75ed2ab9"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Compound index does not currently support nested documents or arrays 

Azure Cosmos DB now supports [composite/compound indexes](https://docs.mongodb.com/manual/core/index-compound/) for all MongoDB api customers on v3.6 server version. Customers can create a compound index by using MongoDB's [createIndex()](https://docs.mongodb.com/manual/reference/method/db.collection.createIndex/) command.

[Check Image](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EWYIMPkNlNhCnGGvo3Lcav8Bjk3-8K4NDp5D_ORhw9-q7g?e=HK8nyU)

However, the default implementation of Compound indexes only supports "top-level" properties. If a customer tries to create a compound index using a "dot-notation" path, the createIndex() command will fail with a "Compound index does not currently support nested documents or arrays" error

[Check Image](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EaGK2ZDEb3pEmKUWdbj19aEBsf4ozhfkOeqBIiMdLFBp4g?e=hf5v29)

## Workaround / Mitigation
While compound indexes on nested paths are blocked for all cases, this restriction can be lifted via a server-side config if no properties in the "dot-notation" paths are arrays.
e.g.  In our above example, the below image shows the list of supported and unsupported document types

[Check Image](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EW78X9pRTDBFlFYa_NPsSncBukdB0Qr8fp6aObU9Sr1kSw?e=YmqCQY)

# Question to ask customers

1. **Please share all the compound Index definitions for all collections for this account?**

<Sample Answer>:  I am using db.orders.createIndex({orderId:1, "orderDate.day": 1});

2. **Is any property in the dot-notation path (excluding the last element) an array? i.e. in the command shared above, is "orderDate" an array field in document stored in the "orders" collection**

<Sample Answer>:  No, orderDate is always an Object/Document in all the documents in the "orders" collection
<Sample Answer>:  Maybe, orderDate is an Object/Document in most cases but could be an array in some cases
<Sample Answer>:  Yes, orderDate is always an Array in all the documents.


**If the answer is Maybe/Yes**, please acknowledge the current limitation to the customer and let them know that the CosmosDB Mongo api team is actively working on fixing this limitation.  Go ahead and close the ticket.

**If the answer is Yes**, follow the steps in the next section

