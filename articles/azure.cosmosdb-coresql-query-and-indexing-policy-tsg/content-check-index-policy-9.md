<properties
	  pageTitle="Check Index Policy"
	  description="Check Index Policy"
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
	  articleId="dab7199a-9a7b-480a-8bf2-3b1b362bc18f"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check Index Policy

In Azure Cosmos DB, every container has an indexing policy that dictates how the container's items should be indexed. The default indexing policy for newly created containers indexes every property of every item and enforces range indexes for any string or number. This allows customer  to get good query performance without having to think about indexing and index management upfront.

Please check with customer their index utilization



