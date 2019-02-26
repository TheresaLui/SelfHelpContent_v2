<properties
	pageTitle="Cosmos Db consistency level"
	description="Cosmos DB Consistency"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="78"
	selfHelpType="resource"
	supportTopicIds="32597504"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="d4c8720b-9acd-4677-9113-3c863fac0cd8"
/>

# Azure Cosmos DB consistency levels

* Review [consistency levels](https://docs.microsoft.com/azure/cosmos-db/consistency-levels) for tradeoffs and guarantees per consistency level. We recommend the default of session consistency for most applications, as it provides a good balance of tradeoffs.
* If you're using session consistency and observe stale reads within a session, then you should validate that the session token is round tripped correctly. That is, you should either use a single Cosmos DB SDK instance per session, or explicitly save/route the session token from responses, and echo them in subsequent requests for the session (for load balanced apps).
* If you're seeing stale results for queries, you should validate that your indexing policy is configured using the consistent mode, in addition to the configured consistency level of the account. See [Indexing Policy](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-indexing-policy).

## **Recommended documents**

* [Tunable data consistency levels in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/consistency-levels)
