<properties
	pageTitle="Data Import, Export (ETL)/Using Azure Databricks"
	description="Data Import, Export (ETL)/Using Azure Databricks"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	supportTopicIds="32635228"
	productPesIds="15818"
	displayOrder="4"
	selfHelpType="generic"
	resourceTags=""
	articleId="dw-dataimportexport-usingazuredatabricks.md"
	cloudEnvironments="public"
/>
# Using Azure Databricks

## **Recommended Steps**
* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL Data Warehouse increases the numbers of readers and writers for parallelism.<br>
* [Load data into SQL Data Warehouse using Azure Databricks](https://docs.microsoft.com/azure/azure-databricks/databricks-extract-load-sql-data-warehouse?toc=/azure/sql-data-warehouse/toc.json)

## **Recommended Documents**
* [Best practices when loading into SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)