<properties
	pageTitle="GridFS exceeding the storage quota issue"
	description="GridFS exceeding the storage quota issue"
	service="Microsoft.DocumentDB"
	resource="databaseAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="41d09c8e-2285-45e8-833b-9c331531ec06"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# GridFS exceeding the storage quota issue

<!--issueDescription-->

Dear customer,

MongoDB GridFS solution is currently built on top of "Attachmaents and media" resource model in CosmosDB so all of its inherit limits apply to Attachments as well. Currently, CosmosDB only support total attachments upto 2GB in size (documented in the above link) and the same restriction also applies to GridFS collections.

To workaround this issue, use Azure Blob storage to store the binary data and then store the file url's into CosmosDB. Split the file on the client side and store into different collection. Customer needs to split the large data into smaller chunks and then use MongoDB api to store the data into a different collection.

Thank you.

<!--/issueDescription-->

