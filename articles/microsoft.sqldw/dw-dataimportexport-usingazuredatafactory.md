<properties
	pageTitle="Data Import, Export (ETL)/Using Azure Data Factory"
	description="Data Import, Export (ETL)/Using Azure Data Factory"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	supportTopicIds="32635226"
	productPesIds="15818"
	displayOrder="4"
	selfHelpType="generic"
	resourceTags=""
	articleId="dw-dataimportexport-usingazuredatafactory.md"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# Using Azure Data Factory

## **Recommended Steps**
* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL Data Warehouse increases the numbers of readers and writers for parallelism.<br>
* [Load data into Azure SQL Data Warehouse by using Azure Data Factory](https://docs.microsoft.com/azure/data-factory/load-azure-sql-data-warehouse?toc=/azure/sql-data-warehouse/toc.json)

## **Recommended Documents**
* [Best practices when loading into SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)