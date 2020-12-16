<properties
	  pageTitle="Cross partition query is required but disabled issue"
	  description="Cross partition query is required but disabled issue"
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
	  articleId="8e9bdd0c-2701-4bf0-aef7-34abf5aba2f4"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Cross partition query is required but disabled issue

<!--issueDescription-->

Dear customer,

If your data was previously distributed using a single partition your queries may have worked even though *EnableCrossPartitionQuery = false*. If your data is now distributed across more than one partition, please enable the crossPartitionQuery by setting enableCrossPartitionQuery=true through code as shown below to resolve the issue.  
`var option = new FeedOptions { EnableCrossPartitionQuery = true };`  

Thank you.

<!--/issueDescription-->

