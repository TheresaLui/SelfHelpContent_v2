<properties
	pageTitle="Storage Size is very large after loading into Cosmos DB Mongo API issue"
	description="Storage Size is very large after loading into Cosmos DB Mongo API issue"
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
	articleId="55622ee0-7490-4ed6-a67e-5d1617ba1168"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Storage Size is very large after loading into Cosmos DB Mongo API issue

<!--issueDescription-->

Dear customer,

The Mongo API in Cosmos DB uses BSON format which is not the native format of Cosmos DB core. The BSON format triggers to adding meta data property for each property in the document. Also, note that each Array items in a document would add meta data property for each item leading to additional storage overhead.

Thank you.

<!--/issueDescription-->

