<properties
	  pageTitle="Change a collection from fixed to unlimited (SQL) issue"
	  description="Change a collection from fixed to unlimited (SQL) issue"
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
	  articleId="1476e699-5040-41f3-a509-09c4884ca912"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Change a collection from fixed to unlimited (SQL) issue

<!--issueDescription-->

Dear customer

The non-partitioned containers are legacy and you should migrate your existing non-partitioned containers to partitioned containers to scale storage and throughput. Azure Cosmos DB provides a system defined mechanism to migrate your non-partitioned containers to partitioned containers. This document explains how all the existing non-partitioned containers are auto-migrated into partitioned containers. You can take advantage of the auto-migration feature only if you are using the V3 version of SDKs in all the languages.

Pleae check the following document for more details:
- https://docs.microsoft.com/en-us/azure/cosmos-db/migrate-containers-partitioned-to-nonpartitioned

Thank you.

<!--/issueDescription-->

