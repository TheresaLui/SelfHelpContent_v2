<properties
	  pageTitle="ExceededTimeLimit Error issue"
	  description="ExceededTimeLimit Error issue"
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
	  articleId="383ddbdf-1e78-4ac6-a72e-eab9d9bb8916"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# ExceededTimeLimit Error issue

<!--issueDescription-->

Dear customer,

The request has exceeded the timeout of 60 seconds of execution.
- One of the causes is when the current allocated request units capacity is not sufficient to complete the request. This can be solved by increasing the request units of that collection or database. 
- In other cases, this error can be worked-around by splitting a large request into smaller ones  
- You can also evaluate if the queries can be optimized further by making effective use of the index  

If you are wanting to delete large amounts of data without impacting RU:
* Consider using TTL (Based on Timestamp): [Expire data with Azure Cosmos DB's API for MongoDB](https://docs.microsoft.com/azure/cosmos-db/mongodb-time-to-live)
* Use Cursor/Batch size to perform the delete. You can fetch a single document at a time and delete it through a loop. This would help you to slowly delete without impacting your production application.

Thank you.

<!--/issueDescription-->

