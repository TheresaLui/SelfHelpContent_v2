<properties
    pageTitle="Data Import, Export (ETL)/Using Azure Data Lake"
    description="Data Import, Export (ETL)/Using Azure Data Lake"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,happynicolle"
    ms.author="saltug,nicw"
    supportTopicIds="32635227"
    productPesIds="15818"
    displayOrder="4"
    selfHelpType="generic"
    resourceTags=""
    articleId="dw-dataimportexport-usingazuredatalake.md"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Using Azure Data Lake

## **Recommended Steps**

* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL Data Warehouse increases the numbers of readers and writers for parallelism.
* [Load from Azure Data Lake Storage Gen1 to SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-load-from-azure-data-lake-store)

## **Recommended Documents**

* [Best practices when loading into Synapse SQL](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)
* [Azure SQL Data Warehouse PolyBase connectivity](https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview#azure-sql-data-warehouse-polybase)
* [Azure Data Factory Managed Identity](https://docs.microsoft.com/azure/data-factory/connector-azure-blob-storage#managed-identity)
