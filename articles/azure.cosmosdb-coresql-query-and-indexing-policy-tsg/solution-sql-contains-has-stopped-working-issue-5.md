<properties
	  pageTitle="SQL CONTAINS has stopped working issue"
	  description="SQL CONTAINS has stopped working issue"
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
	  articleId="8ef6c1a5-715c-436a-8f45-2955b084c333"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# SQL CONTAINS has stopped working issue

<!--issueDescription-->

Dear customer,

If SQL CONTAINS has stopped working in certain instances. The issue can be related with utilizing the index in evaluation Contains expressions directly on the index terms. This has the limitation of truncating the search string once it exceeds 1KB in length. 

As a long ter solution, taking in consideration the length of the _field_ string values, we strongly recommend adding _field_ a path to the excluded path in the indexing policy. This should reduce the size of the index and RUs for inserted documents.

Thank you.

<!--/issueDescription-->

