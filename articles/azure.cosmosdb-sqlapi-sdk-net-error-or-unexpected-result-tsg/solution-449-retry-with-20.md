<properties
	  pageTitle="449 Retry With"
	  description="449 Retry With"
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
	  articleId="9486f7ec-0742-427a-934e-5ef6bbb3191c"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# 449 Retry With

<!--issueDescription-->

Dear customer,

This is an expected response that indicates that there were concurrent operations trying to modify the same document. It is safe to retry. If the error is happening during stored procedure executions, decreasing the degree of parallelism of the executions will also reduce the occurrence.

Thank you.

<!--/issueDescription-->

