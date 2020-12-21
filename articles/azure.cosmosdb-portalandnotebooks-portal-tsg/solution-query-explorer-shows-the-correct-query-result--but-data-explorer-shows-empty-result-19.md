<properties
	  pageTitle="Query explorer shows the correct query result. But Data explorer shows empty result"
	  description="Query explorer shows the correct query result. But Data explorer shows empty result"
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
	  articleId="edee8f38-c8b9-4dd2-bec9-2f2031ceb2dc"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Query explorer shows the correct query result. But Data explorer shows empty result

<!--issueDescription-->

Dear customer,

**Symptom**: Query explorer shows the correct query result. But Data explorer shows empty result.  

**Solution**:
1. Data Explorer only load first partition of data. If the user click ?load more?, he will get all the documents (25 partitions total). This is a known bug in Portal.

2. Please click until you find your document or there is no load more button exist. (up to 25 times) 

Thank you.

<!--/issueDescription-->

