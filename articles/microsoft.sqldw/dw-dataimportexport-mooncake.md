<properties
	pageTitle="How to troubleshoot data import and export issues"
	description="How to troubleshoot data import and export issues"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	supportTopicIds=""
	productPesIds=""
	displayOrder="6"
	selfHelpType="resource"
	resourceTags="datawarehouse"
	articleId="dw-dataimportexport-mooncake"
	cloudEnvironments="MoonCake"
	ownershipId="AzureData_AzureSQLDB"
/>
# How to troubleshoot data import and export issues

## **Recommended Steps**

Always leverage Polybase to batch load into your data warehouse and avoid singleton inserts.

* Use CTAS as opposed to INSERT INTO to avoid full logging into [staging heap tables](https://docs.azure.cn/sql-data-warehouse/design-elt-data-loading) (especially on Gen2) and consider [partition switching](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-tables-partition) to optimize load performance
* Make sure to co-locate your staging area (blob storage or data lake store) and your data warehouse to minimize latency
* Maximize throughput when using gzip text files by splitting files up into 60 or more files to maximize parallelism
* [Use the appropriate resource class and service level](https://docs.azure.cn/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.azure.cn/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL Data Warehouse increases the numbers of readers and writers for parallelism.

## **Recommended Documents**

* [Best practices when loading into SQL Data Warehouse](https://docs.azure.cn/sql-data-warehouse/guidance-for-loading-data)
* [Designing a Polybase data loading strategy for Azure SQL Data Warehouse](https://docs.azure.cn/sql-data-warehouse/design-elt-data-loading#4-load-the-data-into-sql-data-warehouse-staging-tables-using-polybase)