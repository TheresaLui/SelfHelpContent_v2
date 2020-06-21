<properties
	pageTitle="High RU consumption for indexing terms - RCA"
	description="RCA - High RU consumption for indexing terms"
	infoBubbleText="High RU consumption for indexing terms within your documents. See details on the right"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="rnagpal"
	ms.author="rnagpal"
	articleId="cosmosdb-highindexterms-rca"
	selfHelpType="rca"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureCosmosDB"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We found high RU consumption for indexing terms within your documents.
<!--/issueDescription-->
Inserting or updating documents with large number of properties may result in high indexing RUs being consumed as part of document insert or update.

## **Recommended Steps**

### Evaluate encoding non-queryable content
If there are properties/sections in your items that are not queried, but need to be globally distributed or accessed at low latency, e.g. binary content or free text, consider an encoding/compression to reduce their footprint and RU consumption.

### Evaluate custom indexing policy
If your items are dense in content (contain a large number of properties), the RUs consumed for indexing may be high. Every property consumes about 0.15 RUs, and this can add up if you have 100s-1000s of RUs. 

## **Recommended Documents**

See [Indexing policies](https://docs.microsoft.com/azure/cosmos-db/indexing-policies) for more details.
