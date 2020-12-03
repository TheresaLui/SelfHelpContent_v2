<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "sqlPools"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783938"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Data Import, Export (ETL) with Dedicated SQL pool/Using Azure Data Factory, Azure Data Lake Analytics"
    description = "Data Import, Export (ETL) with Dedicated SQL pool/Using Azure Data Factory, Azure Data Lake Analytics"
    articleId = "synapse-cs-dataimportexportetlwithdedicatedsqlpool-usingazuredatafactoryazuredat.md"
    ms.author = "saltug"
/>

# Data Import, Export (ETL) with Dedicated SQL pool/Using Azure Data Factory, Azure Data Lake Analytics

## **Recommended Steps**

* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, Dedicated SQL pool increases the numbers of readers and writers for parallelism.

* [Load data into Dedicated SQL pool by using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/load-azure-sql-data-warehouse?toc=/azure/sql-data-warehouse/toc.json)

* [Load from Azure Data Lake Storage Gen1 to Dedicated SQL pool](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-load-from-azure-data-lake-store)

## **Recommended Documents**

* [Best practices when loading into Dedicated SQL pool](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)

 