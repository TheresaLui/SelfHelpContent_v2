<properties
	  pageTitle="You can see the documents created using 'Query Explorer' but it returns 'no document found',"
	  description="You can see the documents created using 'Query Explorer' but it returns 'no document found',"
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
	  articleId="6c6a2171-36c8-4bd1-90f0-e17ced0d32e9"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# You can see the documents created using 'Query Explorer' but it returns 'no document found',

<!--issueDescription-->

Dear customer,

**Symptom**: You can see the documents created while using 'Query Explorer', but if you take the ID of one of the documents in Data Explorer in order to edit it,  it returns 'no document found.'

**Solution**: This behavior is by design (as of March 2017).

a. The search above the list of documents allows you to find a document in the list of documents already loaded in the portal. The search will find the document only if you have already loaded it from the server.

 Another thing to note is, click on "Load More" (if the button is available) and the document being searched for may show up in the results list.

b. You can specify a filter to apply on the query the portal sends to the server to get fewer documents.

Thank you.

<!--/issueDescription-->

