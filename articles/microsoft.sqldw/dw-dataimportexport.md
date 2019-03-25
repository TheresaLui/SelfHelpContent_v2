<properties
	pageTitle="How to troubleshoot data import and export issues"
	description="How to troubleshoot data import and export issues"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	supportTopicIds="32635179, 32635209, 32635226, 32635227, 32635228, 32635229, 32635230, 32635231"
	productPesIds="15818"
	displayOrder="104"
	selfHelpType="resource"
	resourceTags=""
	articleId="dw-dataimportexport.md"
	cloudEnvironments="public"
/>
# Data Import, Export (ETL)

## **Recommended Steps**
Always leverage Polybase to batch load into your data warehouse and avoid singleton inserts.

* Use CTAS as opposed to INSERT INTO to avoid full logging into [staging heap tables](https://docs.microsoft.com/azure/sql-data-warehouse/design-elt-data-loading) (especially on Gen2) and consider [partition switching](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-tables-partition) to optimize load performance.<br>
* Make sure to co-locate your staging area (blob storage or data lake store) and your data warehouse to minimize latency.<br>
* Maximize throughput when using gzip text files by splitting files up into 60 or more files to maximize parallelism.<br>
* [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL Data Warehouse increases the numbers of readers and writers for parallelism.

## **Recommended Documents**
* [Best practices when loading into SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)<br>
* [Designing a Polybase data loading strategy for Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/design-elt-data-loading#4-load-the-data-into-sql-data-warehouse-staging-tables-using-polybase)