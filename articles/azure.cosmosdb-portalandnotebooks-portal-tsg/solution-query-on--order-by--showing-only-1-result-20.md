<properties
	  pageTitle="Query on "order by" showing only 1 result"
	  description="Query on "order by" showing only 1 result"
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
	  articleId="aa859713-a4df-4505-acee-845d9b5584d3"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Query on "order by" showing only 1 result

<!--issueDescription-->

Dear customer,

**Symptom**: Query explorer with SQL order by clause showing only 1 result  

**Solution**:

"ORDER BY ASC" the query is taking a long time to execute so the results will be returned over multiple continuation. You can see that there is a "load more" button right next to the result count. Clicking on this button will return the next set of records. You need to click on load more till all the 100 records are returned. 

Thank you.

<!--/issueDescription-->

