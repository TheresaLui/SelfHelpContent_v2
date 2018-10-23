  <properties
	pageTitle="How to troubleshoot issues and follow best practices when loading data"
	description="How to build and troubleshoot Extract, Load, Transform (ELT) pipelines"
	service="microsoft.sql"
	resource="servers"
	authors="kevinvngo"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="datawarehouse"
	productPesIds=""
	cloudEnvironments="MoonCake"
/>

# How to troubleshoot issues and follow best practices when loading data

## **Recommended steps**

Always leverage Polybase to batch load into your data warehouse and avoid singleton inserts.

* Use CTAS as opposed to INSERT INTO to avoid full logging into [staging heap tables](https://docs.azure.cn/sql-data-warehouse/design-elt-data-loading) (especially on Gen2) and consider [partition switching](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-tables-partition) to optimize load performance.
* Make sure to co-locate your staging area (blob storage or data lake store) and your data warehouse to minimize latency.
* Maximize throughput when using gzip text files by splitting files up into 60 or more files to maximize parallelism.
* [Use the appropriate resource class and service level](https://docs.azure.cn/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.azure.cn/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL Data Warehouse increases the numbers of readers and writers for parallelism.

## **Recommended documents**

* [Best practices when loading into SQL Data Warehouse](https://docs.azure.cn/sql-data-warehouse/guidance-for-loading-data)
