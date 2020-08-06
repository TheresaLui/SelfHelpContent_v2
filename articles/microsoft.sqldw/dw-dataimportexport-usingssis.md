<properties
    pageTitle="Data Import, Export (ETL)/Using SSIS"
    description="Data Import, Export (ETL)/Using SSIS"
    service="microsoft.sql"
    resource="servers"
    authors="saltug,happynicolle"
    ms.author="saltug,nicw"
    supportTopicIds="32635231"
    productPesIds="15818"
    displayOrder="4"
    selfHelpType="generic"
    resourceTags=""
    articleId="dw-dataimportexport-usingssis.md"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Using SSIS

## **Recommended Steps**

* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL Data Warehouse increases the numbers of readers and writers for parallelism.
* [Load data into SQL Data Warehouse using SSIS](https://docs.microsoft.com/sql/integration-services/load-data-to-sql-data-warehouse?view=sql-server-2017)

## **Recommended Documents**

* [Best practices when loading into SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)
