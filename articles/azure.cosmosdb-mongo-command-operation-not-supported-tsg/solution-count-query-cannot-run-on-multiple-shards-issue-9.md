<properties
	  pageTitle="Count query cannot run on multiple shards issue"
	  description="Count query cannot run on multiple shards issue"
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
	  articleId="ff8d0c74-69cc-4273-ad79-f02f2b748897"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Count query cannot run on multiple shards issue

<!--issueDescription-->

Dear customer,

If you are getting the Count query cannot run on multiple shards, this error is thrown on legacy MongoDB version 3.2 accounts when running a CRUD (Create, Read, Update, Delete) command against a sharded collection and the shard key value is not specified in the command.  This issue is addressed for new Mongo accounts on 3.6.  
If you are experiencing this issue and unable to migrate to 3.6, please consider the following solution:
* Use a combination of Cursor and find to get the required count. Example, for every shard key value from the cursor, modify the find command to contain the shard key field and its value.

Thank you.

<!--/issueDescription-->

