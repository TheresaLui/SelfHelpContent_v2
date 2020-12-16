<properties
	  pageTitle="Long floating-point values in a document are rounded when viewed from data explorer in the portal issue"
	  description="Long floating-point values in a document are rounded when viewed from data explorer in the portal issue"
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
	  articleId="14a23118-9158-42f7-965e-a82c88772a83"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Long floating-point values in a document are rounded when viewed from data explorer in the portal issue

<!--issueDescription-->

Dear customer,

This is limitation of JavaScript. JavaScript uses double-precision floating-point format numbers as specified in IEEE 754 and it can safely hold numbers between -(253 - 1) and 253-1 (i.e., 9007199254740991) only

Link: https://docs.microsoft.com/en-us/azure/cosmos-db/faq#why-are-long-floating-point-values-in-a-document-rounded-when-viewed-from-data-explorer-in-the-portal  

Thank you.

<!--/issueDescription-->

