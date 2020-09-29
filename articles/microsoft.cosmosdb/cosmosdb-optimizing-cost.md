<properties
    pageTitle="Azure Cosmos DB - Optimizing costs"
    description="Azure Cosmos DB - Optimizing costs"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32636802"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-optimizing-cost"
    displayOrder="42"
    category="General Advisory"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB - Optimizing costs

Most users are able to resolve their Optimizing cost issue using the steps and reviewing the recommended documents below.


## **Recommended Steps** 

Azure Cosmos DB resources are charged based on the storage consumed(GB) and the throughput provisioned(RU/s) for a container. Each container with provisioned throughput is billed on an hourly basis for the throughput provisioned in increments of 100 RU/second.  


### **Received a high bill for Cosmos DB QA environment and is looking to reduce the costs?**  
- You may consider creating a shared database and separate containers within the database to reduce costs
- Investigate using [autoscale](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autoscale) 
- Review your queries, are you querying across partitions because it does not contain a partition key?


## **Recommended Documents**
[Pricing model in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-pricing-works)
<br>The pricing model of Azure Cosmos DB simplifies the cost management and planning. With Azure Cosmos DB, you pay for the throughput provisioned and the storage that you consume.  

[Understand your Azure Cosmos DB bill](https://docs.microsoft.com/azure/cosmos-db/understand-your-bill)
<br>This article uses some examples to help you understand the details you see on the monthly bill. The numbers shown in the examples may be different if your Azure Cosmos containers have a different amount of throughput provisioned, if they span across multiple regions or run for a different for a period over a month.  

[Optimize development and testing cost in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/optimize-dev-test)
<br>This article describes the different options to use Azure Cosmos DB for development and testing for free of cost.   

[Total Cost of Ownership(TCO) with Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/total-cost-ownership)
<br>Azure Cosmos DB is designed with the fine grained multi-tenancy and resource governance. This design allows Azure Cosmos DB to operate at significantly lower cost and help users save. Currently Azure Cosmos DB supports more than 280 customer workloads on a single machine with the density continuously increasing, and thousands of customer workloads within a cluster. It load balances replicas of customers' workloads across different machines in a cluster and across multiple clusters within a data center.   

[Optimize provisioned throughput cost in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/optimize-cost-throughput)
<br>You can provision throughput on databases or containers and each strategy can help you save on costs depending on the scenario.  

[Optimize multi-region cost in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/optimize-cost-regions)
<br>Provisioned throughput with single write region costs $0.008/hour per 100 RU/s and provisioned throughput with multiple writable regions costs $0.016/per hour per 100 RU/s.   

[Optimize cost with reserved capacity in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cosmos-db-reserved-capacity)
<br>Azure Cosmos DB reserved capacity can significantly reduce your Cosmos DB costs up to 65 percent on regular prices with a one-year or three-year upfront commitment. Reserved capacity provides a billing discount and does not affect the runtime state of your Azure Cosmos DB resources.  

[Use Azure Cosmos DB autoscale](https://docs.microsoft.com/azure/cosmos-db/provision-throughput-autoscale)
<br>Azure Cosmos DB allows you to set either standard (manual) or autoscale provisioned throughput on your databases and containers. This article describes the benefits and use cases of autoscale provisioned throughput.

With autoscale, Azure Cosmos DB automatically and instantly scales the throughput (RU/s) of your database or container based on usage, without impacting the availability, latency, throughput, or performance of the workload.

[How to enable autoscale](https://docs.microsoft.com/azure/cosmos-db/how-to-provision-autoscale-throughput?tabs=api-async)
<br>You can enable autoscale on existing databases and containers through the Azure portal. To create new databases and containers with autoscale, use the Azure portal, Azure Resource Manager template, or latest versions of the Azure Cosmos DB .NET SDK V3.9+ or Java SDK V4+. See this article for samples. 

