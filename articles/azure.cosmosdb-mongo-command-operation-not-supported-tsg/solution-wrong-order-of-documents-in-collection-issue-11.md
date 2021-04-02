<properties
	  pageTitle="Wrong order of documents in collection issue"
	  description="Wrong order of documents in collection issue"
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
	  articleId="9d332dc1-a222-4e54-af9b-ee9dafab5500"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Wrong order of documents in collection issue

<!--issueDescription-->

Dear customer,

You are getting the issue Wrong order of documents in collection is not being retuned as expected in a find() query. The order of insert is being defined by the _id or ObjectId() field that is auto generated.  or sometimes set in the document. 

#### Solution:
Having an index does not guaranty sorted result. If the you wants sorted result, please use sort function.  db.collfind({}).sort({_id:1}) 

Thank you.

<!--/issueDescription-->

