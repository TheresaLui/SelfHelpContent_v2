<properties
	  pageTitle="Deleting large amounts of data issue"
	  description="Deleting large amounts of data issue"
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
	  articleId="4878b293-5282-4f5d-88ce-964a77319546"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Deleting large amounts of data issue

<!--issueDescription-->

Dear customer,

If you are wanting to delete large amounts of data without impacting RU:
* Consider using TTL (Based on Timestamp) [Expire data with Azure Cosmos DB's API for MongoDB](https://docs.microsoft.com/azure/cosmos-db/mongodb-time-to-live)
* Use Cursor/Batch size to perform the delete. You can fetch a single document at a time and delete it through a loop. This would help you to slowly delete without impacting your production application.

Thank you.

<!--/issueDescription-->

