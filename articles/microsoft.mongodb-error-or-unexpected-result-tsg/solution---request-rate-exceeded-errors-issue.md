<properties
	pageTitle="Request rate exceeded errors issue"
	description="Request rate exceeded errors issue"
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
	articleId="8c53573a-832b-4466-9a10-4a186f76a098"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Request rate exceeded errors issue

<!--issueDescription-->

Dear customer,

Some of the queries including aggregations require a large amount of processing. If the collection's throughput is not enough, you will see these errors. You can confirm this by going to the Metrics blade and selecting the Throughput tab for your collection. You can also evaluate if the queries can be optimized further by making effective use of the index.

If you get a 16500 error(throttling) please increase the value of throughput or use the limit() function to reduce the value of throughput.

As mentined above, please make effective use of the index, Azure Cosmos DB's API for MongoDB 3.6 automatically indexes the _id field only. This default indexing policy differs from the Azure Cosmos DB SQL API, which indexes all fields by default. To index additional fields, you apply the MongoDB index-management commands. After implementing a correct index structure, you should have a considerable decrease in the amount of the RUs.

Thank you.

<!--/issueDescription-->

