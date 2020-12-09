<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "sqlPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783863"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "How-To/Dedicated SQL pool - Loading Data"
    description = "How-To/Dedicated SQL pool - Loading Data"
    articleId = "synapse-cs-howto-dedicatedsqlpoolloadingdata.md"
    ms.author = "saltug"
/>

# How-To/Dedicated SQL pool - Loading Data

## **Recommended Steps**

Always leverage Polybase to batch load into your Dedicated SQL pool and avoid singleton inserts.

* Use CTAS as opposed to INSERT INTO to avoid full logging into [staging heap tables](https://docs.microsoft.com/azure/sql-data-warehouse/design-elt-data-loading) (especially on Gen2) and consider [partition switching](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-tables-partition) to optimize load performance

* Make sure to co-locate your staging area (blob storage or data lake store) and your Dedicated SQL pool to minimize latency

* Maximize throughput when using gzip text files by splitting files up into 60 or more files to maximize parallelism

* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL pool increases the numbers of readers and writers for parallelism.

## **Recommended Documents**

* [Best practices when loading into Dedicated SQL pool](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)

* [Designing a Polybase data loading strategy for Dedicated SQL pool](https://docs.microsoft.com/azure/sql-data-warehouse/design-elt-data-loading#4-load-the-data-into-sql-data-warehouse-staging-tables-using-polybase)

 