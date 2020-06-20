<properties
    pageTitle="Autoscale"
    description="Troubleshoot Azure Cosmos DB throughput autoscale issues"
    service="microsoft.documentdb" 
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32692540"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-throughput-autopilot"
    displayOrder="247"
    category="Core (SQL)"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB autoscale provisioned throughput
Use the below solutions to solve common issues with autoscale.

## **Recommended Steps**

### **How do I know the current RU/s autoscale has scaled to?**  
In Azure Monitor metrics, the [**Provisioned Throughput**](https://docs.microsoft.com/azure/cosmos-db/how-to-choose-offer#measure-and-monitor-your-usage) metric represents the current RU/s the system has scaled to. This metric is emitted every 5 minutes and shows the highest RU/s in the 5 minute interval. You will be billed for the highest RU/s the system scaled to within each hour. If there is no usage, you will be billed for the minimum of ``0.1 * Max RU/s``. 

When you create a database or container with autoscale, Azure Cosmos DB initially provisions the underlying physical partitions needed so that at any moment, you can use up to the max RU/s at any time with no delay. 

### **Unable to switch between autoscale and manual throughput**  
Azure Cosmos DB supports switching between autoscale and manual provisioned throughput. Currently, you can only use the Azure portal to do this operation. 

PowerShell and CLI support is planned, but not yet available. 

If you are unable to do this operation via the Azure portal, and you have greater than 100,000 RU/s on a resource, file a support ticket under the **Limits and quotas** category. 

### **Unable to lower RU/s beyond the minimum**  
When you lower the max RU/s, the minimum value you can set it to is: MAX(4000, highest max RU/s ever provisioned / 10, current storage in GB * 100), rounded to the nearest 1000 RU/s.

For a shared throughput database, when you lower the max RU/s, the minimum value you can set it to is: MAX(4000, highest max RU/s ever provisioned / 10, current storage in GB * 100, 4000 + (MAX(Container count - 25, 0) * 1000)), rounded to the nearest 1000 RU/s.

You can find the history of autoscale max RU/s and storage in Azure Monitor metrics. 

The above formulas and examples relate to the minimum autoscale max RU/s you can set, and is distinct from the 0.1 * Tmax to Tmax range the system automatically scales between. No matter what the max RU/s is, the system will always scale between 0.1 * Tmax to Tmax. [Learn more.](https://docs.microsoft.com/azure/cosmos-db/autoscale-faq#lowering-the-max-rus)

### **Why am I getting throttled or seeing 429s with autoscale?**  
It is possible to see 429s in two scenarios. 

First, if you use more than the max RU/s, the service will throttle requests accordingly. 

Second, you'll see 492s if you have a hot partition. Hot partitions occur when you have logical partition key value that has a disproportionately higher amount of requests compared to other partition key values. For example, if you partition by "companyName", and most your operations only write or query on one specific company, "Contoso" there is a hot partition on the "Contoso" partition key value. 

To see if you have a hot partition, use [Azure Monitor metrics](https://docs.microsoft.com/azure/cosmos-db/monitor-normalized-request-units) to see normalized utilization by physical partition. If one or a few physical partitions consistently have much higher utilization than others, there is a hot partition. 

You will see 429s if the underlying physical partition a logical partition key resides in exceeds 100% normalized utilization. 

 As a best practice, to avoid hot partitions, [choose a good partition key](https://docs.microsoft.com/azure/cosmos-db/partitioning-overview#choose-partitionkey) that results in an even distribution of both storage and throughput. If you need to change your partition key, see this [article](https://devblogs.microsoft.com/cosmosdb/how-to-change-your-partition-key/) for instructions.

### **How do I work with autoscale programatically?**  

Currently, you can enable autoscale on an existing database or container only through the Azure portal.

To create or manage new resources with autoscale, use the Azure portal, Azure Resource Manager, or the latest version of the .NET V3 SDK and Java V4 SDK. Support in Azure CLI, PowerShell, and other SDKs is planned, but not yet available.

### **Why did the autoscale max RU/s change as storage increased?**  
For any value of max RU/s ``Tmax``, the database or container can store a total of ``0.01 * Tmax GB``. After this amount of storage is reached, the maximum RU/s will be automatically increased based on the new storage value, with no impact to your application.

For example, if you start with a maximum RU/s of 50,000 RU/s (scales between 5000 - 50,000 RU/s), you can store up to 500 GB of data. If you exceed 500 GB - e.g. storage is now 600 GB, the new maximum RU/s will be 60,000 RU/s (scales between 6000 - 60,000 RU/s).

When you use database level throughput with autoscale, you can have the first 25 containers share an autoscale maximum RU/s of 4000 (scales between 400 - 4000 RU/s), as long as you don't exceed 40 GB of storage. 

[Learn more](https://docs.microsoft.com/azure/cosmos-db/autoscale-faq#can-i-change-the-max-rus-on-the-database-or-container).

### **Does Free Tier discount work with autoscale databases and containers?**
**Answer:** Yes. With autoscale, you are billed for the highest RU/ss the database or container scales to in the hour. When the free tier discount is applied, 400 RU/s will be subtracted from that value. See our [documentation](https://docs.microsoft.com/azure/cosmos-db/understand-your-bill#billing-examples-with-free-tier-accounts) for examples and details.  

### **How many containers can I have in a shared throughput database with autoscale?**
You can have up to 25 containers in a shared throughput database in Azure Cosmos DB, including databases with autoscale.

## **Recommended Documents**  

[Autoscale FAQ](https://docs.microsoft.com/azure/cosmos-db/autoscale-faq)
<br>This article covers commonly asked questions about Azure Cosmos DB autoscale

[How to enable autoscale](https://docs.microsoft.com/azure/cosmos-db/how-to-provision-autoscale-throughput?tabs=api-async)
<br>You can enable autoscale on existing resources through the Azure portal, or use the Azure Resource Manager, or latest versions of the Azure Cosmos DB .NET SDK V3.9+ or Java SDK V4+. See this article for samples. 

[How to choose between manual and autoscale](https://docs.microsoft.com/azure/cosmos-db/how-to-choose-offer)
<br>This article describes how to choose between standard (manual) and autoscale provisioned throughput. Learn how to understand your traffic patterns, monitor your existing applications, and determine if autoscale can help. 