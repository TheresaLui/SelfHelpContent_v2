<properties
	  pageTitle="Support for geospatial operators issue"
	  description="Support for geospatial operators issue"
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
	  articleId="a35a69bf-572e-4f64-8c4e-0694a049e5a3"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Support for geospatial operators issue

<!--issueDescription-->

Dear customer,

You are trying to Migrate your data to CosmosDB MongoDB as it now supports Geospatial operators.
But the indexing does not allow "2d" mode. However, "2dsphere" is allowed.

#### Resolution:
At this time we support "2dsphere" and plan to support "2d" in the future.  

Please review https://docs.mongodb.com/manual/geospatial-queries/#geospatial-indexes as you'll need most likely be better served using "2dsphere"

Thank you .

<!--/issueDescription-->

