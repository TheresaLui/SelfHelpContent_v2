<properties
	  pageTitle="ExceededMemoryLimit issue"
	  description="ExceededMemoryLimit issue"
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
	  articleId="6a689a11-0aef-47bf-ac71-5ff8bc0bbf1d"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# ExceededMemoryLimit issue

<!--issueDescription-->

Dear customer,

As a multi-tenant service, if you receive this error it means the operation has gone over the client's memory allotment. This error is specific to server version 3.2 and will not be encountered on accounts on server version 3.6.  
Steps to correct for version 3.2:
* Reduce the scope of the operation through more restrictive query criteria 
<br>Example: *db.getCollection('users').aggregate([{$match: {name: "Andy"}}, {$sort: {age: -1}}]))*  

Thank you.

<!--/issueDescription-->

