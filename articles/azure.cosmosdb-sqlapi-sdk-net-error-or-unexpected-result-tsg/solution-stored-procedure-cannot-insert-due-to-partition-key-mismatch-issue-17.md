<properties
	  pageTitle="Stored procedure cannot insert due to partition key mismatch issue"
	  description="Stored procedure cannot insert due to partition key mismatch issue"
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
	  articleId="49c76659-166a-4938-87bb-921825976bc6"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Stored procedure cannot insert due to partition key mismatch issue

<!--issueDescription-->

Dear customer,

CancellationToken parameter in ExecuteStoredProcedureAsync should be given as the 3rd parameter. If it is not the payload will be incorrect. 

Thank you.

<!--/issueDescription-->

