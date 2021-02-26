<properties
	  pageTitle="Using UpsertItem issue"
	  description="Using UpsertItem issue"
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
	  articleId="7b4356a4-5f55-4eb2-bf6f-7ab288bf6c3d"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Using UpsertItem issue

<!--issueDescription-->

Dear customer,

If *sys_id* is different for the item that is being used in the *upsert* call, then it will create a new item even if the *id* is same. Uniqueness of an item depends on *id* + *partitionkey* together.  Please see [UpsertItem documentation](https://docs.microsoft.com/python/api/azure-cosmos/azure.cosmos.cosmos_client.cosmosclient?view=azure-python#upsertitem-database-or-container-link--document--options-none-).

Thank you.

<!--/issueDescription-->

