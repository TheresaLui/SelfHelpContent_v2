<properties
	  pageTitle="Azure Functions does not work as expected issue"
	  description="Azure Functions does not work as expected issue"
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
	  articleId="a1729b6e-32b8-4502-b7aa-0e14fece913b"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Functions does not work as expected issue

<!--issueDescription-->

Dear customer,

We have made a recent change to block cross API access. The change is only enabled for new mongo accounts. With this flag enabled, a mongo account could not be accessed with DocumentDB SDK (or change feed reader)for data operations. Management operations (offer replace/ Database creation/Collections creation) are still allowed. The change will impact Azure functions as it uses change feed reader behind the scene.

Thank you.

<!--/issueDescription-->

