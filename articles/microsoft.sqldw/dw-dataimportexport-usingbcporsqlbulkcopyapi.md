<properties
    pageTitle="Data Import, Export (ETL)/Using bcp or SQLBulkCopy API"
    description="Data Import, Export (ETL)/Using bcp or SQLBulkCopy API"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,mlee3gsd"
    ms.author="saltug,martinle"
    supportTopicIds="32635229"
    productPesIds="15818"
    displayOrder="4"
    selfHelpType="generic"
    resourceTags=""
    articleId="dw-dataimportexport-usingbcporsqlbulkcopyapi.md"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Using bcp or SQLBulkCopy API

## **Recommended Steps**

* If you cannot use PolyBase to load and must use the SQLBulkCopy API (or BCP), you should consider increasing batch size for better throughput.
* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL Data Warehouse increases the numbers of readers and writers for parallelism.
* When loading using BCP, make sure you specify the -q parameter to set the QUOTED_IDENTIFIERS on
* [Using bcp or SQLBulkCopy API to load data into SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/design-elt-data-loading#4-load-the-data-into-sql-data-warehouse-staging-tables-using-polybase)

## **Recommended Documents**

* [Best practices when loading into SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)
