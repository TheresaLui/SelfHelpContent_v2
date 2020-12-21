<properties
	  pageTitle="Date header doesn't conform to the required format"
	  description="Date header doesn't conform to the required format"
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
	  articleId="c9abc0fb-3ea1-4ef0-bb0b-b104123b351e"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Date header doesn't conform to the required format

<!--issueDescription-->

Dear customer,

The Cosmos DB SDK has a dependency on joda-time lib 2.9.9. Reference the Maven Artifact: Java SDK for SQL API of Microsoft Azure Cosmos DB .
If you are using an older version of joda-time < 2.9.9 (maybe as a transitive dependency by another dependency) You may encounter this issue.

Verify you are using the correct version of joda-time and explicitly setting the dependency for joda-time 2.9.9 will resolve the issue
The read session is not available for the input session token
You receive an exception The read session is not available for the input session token

You need to upgrade your SDK version

Thank you.

<!--/issueDescription-->

