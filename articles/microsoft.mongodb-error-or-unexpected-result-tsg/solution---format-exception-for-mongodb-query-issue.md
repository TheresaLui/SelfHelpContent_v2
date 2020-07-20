<properties
	pageTitle="Format Exception for MongoDB query issue"
	description="Format Exception for MongoDB query issue"
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
	articleId="cfc50f96-0d71-4674-994d-18e99b430d31"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Format Exception for MongoDB query issue

<!--issueDescription-->

Dear customer,

You cannot use Cosmos DB SDKs to add documents to a Mongo account. This is blocked on newer accounts, however, if the account is old enough that the block is not present. You must delete the documents you added using the Cosmos DB SQL SDK, using that SDK. They will not be retrievable through the Mongo API. Use Mongo SDKs/drivers to insert documents to Mongo accounts.

<!--/issueDescription-->
