<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "sqlPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783940"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Data Import, Export (ETL) with Dedicated SQL pool/Using bcp or SQLBulkCopy API"
    description = "Data Import, Export (ETL) with Dedicated SQL pool/Using bcp or SQLBulkCopy API"
    articleId = "synapse-cs-dataimportexportetlwithdedicatedsqlpool-usingbcporsqlbulkcopyapi.md"
    ms.author = "saltug"
/>

# Data Import, Export (ETL) with Dedicated SQL pool/Using bcp or SQLBulkCopy API

## **Recommended Steps**

* If you cannot use PolyBase or the [COPY statement](https://docs.microsoft.com/sql/t-sql/statements/copy-into-transact-sql?view=azure-sqldw-latest) to load and must use the SQLBulkCopy API (or BCP), you should consider increasing batch size for better throughput.

* When loading using BCP, make sure you specify the -q parameter to set the QUOTED_IDENTIFIERS on

* Use [the appropriate resource class and service level](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, Dedicated SQL pool increases the numbers of readers and writers for parallelism.

* See the following documentation for more details: [Using bcp or SQLBulkCopy API to load data into Dedicated SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/design-elt-data-loading#4-load-the-data-into-sql-data-warehouse-staging-tables-using-polybase)

## **Recommended Documents**

* [Best practices when loading into Dedicated SQL pool](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/guidance-for-loading-data)

 