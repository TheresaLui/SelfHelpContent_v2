<properties
	pageTitle="Metadata operations RCA"
	description="RCA - High number of metadata operations on collection"
	infoBubbleText="Found information related to Machine Key Status. See details on the right."
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathb"
	displayOrder=""
	articleId="metadatacritical_43DFF466-CDE2-4319-95F7-92FF92B302A4"
  diagnosticScenario="MachineKeyUpdates"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We found a high number of metadata operations on your account
<!--/issueDescription-->
In Cosmos DB, data is distributed across partitions. This includes metadata about your databases/collections as well. Metadata for Cosmos DB has a limited system-reserved RU limit. You can avoid rate limiting from metadata operations by following these patterns.

### Use static Cosmos DB client instances
The Cosmos DB SDK on initialization of the `DocumentClient` constructor fetches metadata about the account including consistency level, databases, collections, partitions, and offers. This initialization may consume a high number of RUs, and must be performed infrequently. Use a single DocumentClient instance and use it for the lifetime of your application.

### Cache the names of databases/collections
Retrieve the names of your databases and collections from configuration or cache them on start. Calls like `readDatabase` or `queryDatabases` will result in calls to the service, and will consume RUs. They must be performed infrequently, i.e. not on every call. 

For other tips on performance and SDK best practices, please see [.NET tips](https://docs.microsoft.com/en-us/azure/cosmos-db/performance-tips) and [Java tips](https://docs.microsoft.com/en-us/azure/cosmos-db/performance-tips-java).