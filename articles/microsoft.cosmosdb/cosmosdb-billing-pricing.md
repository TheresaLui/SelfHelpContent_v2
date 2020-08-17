<properties
    pageTitle="Billing and Pricing"
    description="Troubleshoot Azure Cosmos DB Billing and Pricing issues"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32636791,32741540,32636826"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-billing-pricing"
    displayOrder="100"
    category="Billing and Pricing"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Pricing in Azure Cosmos DB  
Most users are able to resolve their Billing and Pricing case using the steps below.  

## **Recommended Steps**  

Azure Cosmos DB resources are charged based on the storage consumed(GB) and the throughput provisioned(RU/s) for a container. Each container with provisioned throughput is billed on an hourly basis for the throughput provisioned in increments of 100 RU/second.  


### **How does the Free Tier discount show up on my bill?** 
In Free Tier accounts, you will get the first 400 RUs and 5 GB of storage in your account for free. Any RUs and storage beyond 400 RUs and 5 GB will be billed at the regular pricing rates per the pricing page. On the bill, you will not see a charge or line item for the free 400 RUs and 5 GB, only the RUs and storage beyond what is covered by free tier.


## **Recommended Documents**  

[Azure Cosmos DB pricing](https://azure.microsoft.com/pricing/details/cosmos-db/)
<br>This article provides Azure Cosmos DB Price and Cost estimation, and how cost are calculated.  

[Estimate Request Units and Data Storage](https://cosmos.azure.com/capacitycalculator/)
<br>Calculator to assist you in estimating your account configured capacity.

[Request Units in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/request-units)
<br>This article provides details regarding request units (RUs) and the factors you should consider when calculating your provisioned throughput.  

[Billing and Pricing FAQs](https://azure.microsoft.com/pricing/details/cosmos-db/#faqs)
<br>Frequently Asked Billing and RU Questions.  

[Billing Examples with Free Tier Accounts](https://docs.microsoft.com/azure/cosmos-db/understand-your-bill#billing-examples-with-free-tier-accounts)
- Free Tier Billing example - container or database with provisioned throughput
- Free Tier Billing example - container or database with autoscale throughput
- Free Tier Billing example - multi-region, single write region account
- Free Tier Billing example - multi-region, multi-master (multiple write region) account
