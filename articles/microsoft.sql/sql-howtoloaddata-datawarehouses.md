  <properties
	pageTitle="How to troubleshoot issues and follow best practices when loading data"
	description="How to build and troubleshoot Extract, Load, Transform (ELT) pipelines"
	service="microsoft.sql"
	resource="servers"
	authors="kevinvngo"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32412150,32412152, 32412156,32412151"
	resourceTags="datawarehouse"
	productPesIds="15818"
	cloudEnvironments="public"
/>

# How to troubleshoot issues and follow best practices when loading data into your data warehouse

## **Recommended steps**
1. Always leverage Polybase to batch load into your data warehouse and avoid singleton inserts.

  * Use CTAS as opposed to INSERT INTO to avoid full logging into [staging heap tables](https://docs.microsoft.com/azure/sql-data-warehouse/design-elt-data-loading) (especially on Gen2) and consider [partition switching](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-tables-partition) to optimize load performance.
  * Make sure to co-locate your staging area (blob storage or data lake store) and your data warehouse to minimize latency.
  * Maximize throughput when using gzip text files by splitting files up into 60 or more files to maximize parallelism.
  * [Use the appropriate resource class and service level](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data) to ensure [enough memory](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data#loading-to-a-staging-table). As you scale your service level, SQL Data Warehouse increases the numbers of readers and writers for parallelism.


## **Recommended documents**

[Best practices when loading into SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/guidance-for-loading-data)<br>

