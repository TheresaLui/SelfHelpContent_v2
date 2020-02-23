<properties
	pageTitle="Billing and Pricing"
	description="Troubleshoot Azure Cosmos DB Billing and Pricing issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636791,32636806,32636826"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-billing-pricing"
	displayOrder="100"
	category="Billing and Pricing"
/>

# Pricing in Azure Cosmos DB  
Most users are able to resolve their Billing and Pricing case using the steps below.  

## **Recommended Steps**  

Azure Cosmos DB resources are charged based on the storage consumed(GB) and the throughput provisioned(RU/s) for a container. Each container with provisioned throughput is billed on an hourly basis for the throughput provisioned in increments of 100 RU/second.  

## **Recommended Documents**  

[Azure Cosmos DB pricing](https://azure.microsoft.com/pricing/details/cosmos-db/)
<br>This article provides Azure Cosmos DB Price and Cost estimation, and how cost are calculated.  

[Estimate Request Units and Data Storage](https://www.documentdb.com/capacityplanner)
<br>Calculator to assist you in estimating your account configured capacity.

[Request Units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
<br>This article provides details regarding request units (RUs) and the factors you should consider when calculating your provisioned throughput.  

[Billing and Pricing FAQs](https://azure.microsoft.com/pricing/details/cosmos-db/#faqs)
<br>Frequently Asked Billing and RU Questions.