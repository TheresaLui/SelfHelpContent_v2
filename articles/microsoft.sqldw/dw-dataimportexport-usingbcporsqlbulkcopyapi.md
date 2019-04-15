<properties
	pageTitle="Data Import, Export (ETL)/Using bcp or SQLBulkCopy API"
	description="Data Import, Export (ETL)/Using bcp or SQLBulkCopy API"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	supportTopicIds="32635229"
	productPesIds="15818"
	displayOrder="4"
	selfHelpType="generic"
	resourceTags=""
	articleId="dw-dataimportexport-usingbcporsqlbulkcopyapi.md"
	cloudEnvironments="public"
/>
# Using bcp or SQLBulkCopy API

## **Recommended Steps**
* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL Data Warehouse increases the numbers of readers and writers for parallelism.<br>
* [Using bcp or SQLBulkCopy API to load data into SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/design-elt-data-loading#4-load-the-data-into-sql-data-warehouse-staging-tables-using-polybase)

## **Recommended Documents**
* [Best practices when loading into SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)