<properties
	  pageTitle="Bad indexes issues"
	  description="Bad indexes issues"
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
	  articleId="05a83d76-04d0-488e-b481-af18b97bb6c0"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Bad indexes issues

<!--issueDescription-->

Dear customer,

If you are getting Queries that do not utilize index or act as if index does not exist.  

###Cause
Internal index specification has improved from 3.2 and may be out of date.

###Diagnosis
```
db.runCommand({customAction:"GetCollection", collection:"<collectionName>", showIndexes:true})
```
Indexes are out of date if any indexes show requiresReIndex=true.

###Mitigation
Do one of the following  
?	Run the reIndex command  
?	Drop and re-add the index  

**Notes:**    
The reIndex command effectively drops and re-adds the bad indexes which may impact query performance and the ability to sort while the indexes are rebuilt.  We recommend scheduling a time to minimized impact.  


Thank you .

<!--/issueDescription-->

