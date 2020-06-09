<properties
	pageTitle="How to enhance and troubleshoot query performance and execution"
	description="How to enhance and troubleshoot query performance and execution"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,mlee3gsd"
	ms.author="saltug,martinle"
	supportTopicIds=""
	productPesIds=""
	displayOrder="10"
	selfHelpType="resource"
	resourceTags="datawarehouse"
	articleId="dw-performanceandqueryexecution-mooncake"
	cloudEnvironments="MoonCake"
	ownershipId="AzureData_AzureSQLDB"
/>
# How to enhance and troubleshoot query performance and execution

The following details explain how to model and design your data warehouse:

* We recommend reviewing the SQL Data Warehouse [cheat sheet](https://docs.azure.cn/sql-data-warehouse/cheat-sheet) as you begin designing your data warehouse
* [Table design documentation](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-tables-overview#determine-table-category)
* [Query design documentation](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-develop-dynamic-sql)

## **Recommended Steps**

The following are the most common issues for slow query performance:

1. Ensure [table statistics are created and kept up to date](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-tables-statistics#updating-statistics). SQL Data Warehouse does not currently support automatic creation or update of statistics. As you load data into your data warehouse, query plans can regress if statistics are not up to date.

	* The SQL Data Warehouse query optimizer is a cost-based optimizer. It compares the cost of various query plans, and then chooses the plan with the lowest cost, which is in most cases the plan that executes the fastest. The cost-based optimized relies on table statistics to ensure the most optimized query plan is selected.

2. Ensure you consistently have [high quality row groups](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-best-practices#optimize-clustered-columnstore-tables) and [rebuild your indexes to improve rowgroup quality](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-tables-index#rebuilding-indexes-to-improve-segment-quality). Use the appropriate resource class, service level, and an appropriate number of partitions as you load data into your data warehouse to prevent [poor columnstore index quality](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-tables-index#causes-of-poor-columnstore-index-quality).

	* A row group is a chunk of rows that are compressed together in columnstore. To get full speed from your data warehouse, it is important to maximize columnstore row group quality. For best compression and index efficiency, the columnstore index needs to compress the maximum of 1,048,576 rows into each rowgroup.

3. Reduce query data movement operations by [investigating your query plan](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-manage-monitor#monitor-query-execution). You can have a suboptimal plan with:

	* A poor selection of a table distribution key causing [data skew](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-tables-distribute#how-to-tell-if-your-distribution-column-is-a-good-choice)
	* Broadcast move operations which can be avoided by [replicating certain tables](https://docs.azure.cn/sql-data-warehouse/design-guidance-for-replicated-tables#convert-existing-round-robin-tables-to-replicated-tables)

4. Monitor to [ensure your query is not queued](https://docs.azure.cn/sql-data-warehouse/analyze-your-workload#queued-query-detection-and-other-dmvs) and your data warehouse has enough concurrency slots

	* SQL Data Warehouse has a fixed number of concurrency slots depending on the current service level. Queries require several concurrently slots based on their resource class to ensure adequate resources are provided for optimal and efficient query performance. They become queued when there are not enough [slots available](https://docs.azure.cn/sql-data-warehouse/memory-and-concurrency-limits#concurrency-maximums).

5. Ensure [enough tempdb and memory have been allocated](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-manage-monitor#monitor-tempdb) during query execution

	* It is recommended to scale if you see your datawarehouse is close to maxing out its tempdb capacity during high activity. Tempdb is used as a staging area for data movement operations as well as when a queryreaches its memory grant.
	* Each query has a specific memory grant depending on its resource class and the data warehouse service level. When queries consume their grant, they must spill into tempdb slowing down query performance.

6. Avoid directly issuing queries against external tables by [loading data first](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-best-practices#load-then-query-external-tables):

	* External tables are not optimal for queries. External tables residing in Blob storage or Azure data lake does not have compute resources backing them; there the data warehouse cannot offload this work. Therefore, your data warehouse will be required to read the entire file into tempdb to scan the data.


## **Recommended Documents**

* [SQL Data Warehouse Cheat Sheet](https://docs.azure.cn/sql-data-warehouse/cheat-sheet)
* [Investigate Queries with DMVs](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-manage-monitor)
* [Additional Troubleshooting](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-troubleshoot)
