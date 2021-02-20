<properties
	  pageTitle="Index Policy issue"
	  description="Index Policy issue"
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
	  articleId="cd44430c-b294-4e22-9d4e-bb2c262a3670"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Index Policy issue

<!--issueDescription-->

Dear customer,

Index Policy Settings is used to override the default indexing policy on an Azure Cosmos container.

**Note**: This Setting is not available for Mongo or Cassandra accounts.
- Missing Index Policy for Mongo and Cassandra is by Design
- Secondary Indexes on Cosmos DB Cassandra API is not supported

The Index Policy Section under Scale & Setting Tab would be not available for all Mongo and Cassandra Account in the portal.     This behaviour is by design and was made intentionally for all Mongo and Cassandra Accounts.

Please see the document below on how to Index the Azure Cosmos DB MongoDB API:
- https://docs.microsoft.com/en-us/azure/cosmos-db/index-policy
- https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-indexing

Thank you.

<!--/issueDescription-->

