<properties
	  pageTitle="Cannot view my MongoDB API data"
	  description="Cannot view my MongoDB API data"
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
	  articleId="14980cf9-5de9-4e0e-bfbb-3af81ca7f16d"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Cannot view my MongoDB API data

<!--issueDescription-->

Dear customer,

* The Data Explorer uses the native SDK based on the Azure Cosmos DB Account API type to access the data from the service
* Using the Azure Cosmos DB SQL API SDK to perform CRUD operations against a MongoDB API account will not generate any errors. However, this would make the Data Explorer produce the internal server error when reading the data due to a mismatch in the data formats.
* Use the native MongoDB SDKs to perform CRUD operations against your Azure Cosmos DB MongoDB API account  

Thank you.

<!--/issueDescription-->

