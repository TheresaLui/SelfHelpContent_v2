<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "sqlPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783943"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Data Import, Export (ETL) with Dedicated SQL pool/Using Polybase"
    description = "Data Import, Export (ETL) with Dedicated SQL pool/Using Polybase"
    articleId = "synapse-cs-dataimportexportetlwithdedicatedsqlpool-usingpolybase.md"
    ms.author = "saltug"
/>

# Data Import, Export (ETL) with Dedicated SQL pool/Using Polybase

## **Recommended Steps**

Always leverage Polybase to batch load into your Dedicated SQL pool and avoid singleton inserts.

* For an overview on data loading with Dedicated SQL pool, refer to this [documentation](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/design-elt-data-loading)

* Use CTAS as opposed to INSERT INTO to avoid full logging into [staging heap tables](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/design-elt-data-loading) (especially on Gen2) and consider [partition switching](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-tables-partition) to optimize load performance

* Make sure to co-locate your staging area (blob storage or data lake store) and your Dedicated SQL pool to minimize latency

* Maximize throughput when using gzip text files by splitting files up into 60 or more files to maximize parallelism

* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, Dedicated SQL pool increases the numbers of readers and writers for parallelism.

* Load using Managed Identities (MSIs) by visiting the following [documentation](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/load-data-from-azure-blob-storage-using-polybase#authenticate-using-managed-identities-to-load-optional)

* PolyBase can only read UTF8 and UTF16-LE encoded delimited text files

* Monitor progress of your load by visiting the following [documentation](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-manage-monitor#monitor-polybase-load)

* If you encounter Java exception errors such as 105019 with the following error message, "This request is not authorized to perform this operation using this permission", make sure you have properly set up your database scoped credential and data source for your storage account. Ensure you have selected the proper storage account key, provided the appropriate RBAC role(s), or provided the appropriate SQL permissions (CONTROL) to load. 

* If you run into the following error message, "HdfsBridge::recordReaderFillBuffer - Unexpected error encountered filling record reader buffer: HadoopExecutionException: Too many columns in the line", check if you have the proper string delimiter in your external table definition. 

## **Recommended Documents**

* [Best practices when loading into Dedicated SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/guidance-for-loading-data)

* [Designing a Polybase data loading strategy for Dedicated SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/design-elt-data-loading#4-load-the-data-into-sql-data-warehouse-staging-tables-using-polybase)

 