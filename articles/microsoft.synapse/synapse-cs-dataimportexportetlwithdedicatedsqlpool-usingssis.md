<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "sqlPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783944"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Data Import, Export (ETL) with Dedicated SQL pool/Using SSIS"
    description = "Data Import, Export (ETL) with Dedicated SQL pool/Using SSIS"
    articleId = "synapse-cs-dataimportexportetlwithdedicatedsqlpool-usingssis.md"
    ms.author = "saltug"
/>

# Data Import, Export (ETL) with Dedicated SQL pool/Using SSIS

## **Recommended Steps**

* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, Dedicated SQL pool increases the numbers of readers and writers for parallelism.

* [Load data into Dedicated SQL pool using SSIS](https://docs.microsoft.com/sql/integration-services/load-data-to-sql-data-warehouse?view=sql-server-2017)

## **Recommended Documents**

* [Best practices when loading into Dedicated SQL pool](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)

 