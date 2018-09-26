<properties
	pageTitle="Testing BCDR or HADR with Cosmos DB"
  description="Testing BCDR or HADR with Cosmos DB"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="80"
	selfHelpType="resource"
	supportTopicIds="32597525"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>
# How to test BCDR (Business Continuity and Disaster Recovery) or HADR (High Availability and Disaster Recovery) with Azure Cosmos DB

Most enterprise applications include business continuity test as part of their development and release process. BCDR and HADR testing 
is often an important step in compliance certifications and guarantees service availability in the case of regional outages.
You can test the BCDR readiness of your applications that use Azure Cosmos DB by triggering a manual failover of your Cosmos DB account and/or by adding and removing a region dynamically.

## **Recommended documents**

* [Automatic regional failover for business continuity in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/regional-failover)
