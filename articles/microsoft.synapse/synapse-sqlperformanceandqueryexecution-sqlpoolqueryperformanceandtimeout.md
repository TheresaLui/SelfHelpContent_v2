<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "sqlPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738821"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "SQL Performance and Query Execution/SQL pool query performance and timeout"
	description = "SQL Performance and Query Execution/SQL pool query performance and timeout"
	articleId = "synapse-sqlperformanceandqueryexecution-sqlpoolqueryperformanceandtimeout"
	authors = "saltug"
	ms.author = "saltug"
/>

# SQL Performance and Query Execution/SQL pool query performance and timeout

## **Recommended Steps**

The following are the most common issues for slow query performance:

1. Ensure [table statistics are created and kept up to date](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-tables-statistics#updating-statistics). SQL Data Warehouse supports automatic statistics creation and manual statistics updates by users. As you load data into your data warehouse, query plans can regress if statistics are not up to date.

    * The SQL Data Warehouse query optimizer is a cost-based optimizer. It compares the cost of various query plans, and then chooses the plan with the lowest cost, which is in most cases the plan that executes the fastest. The cost-based optimized relies on table statistics to ensure the most optimized query plan is selected.

2. Ensure you consistently have [high quality row groups](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-best-practices#optimize-clustered-columnstore-tables) and [rebuild your indexes to improve rowgroup quality](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-tables-index#rebuilding-indexes-to-improve-segment-quality). Use the appropriate resource class, service level, and an appropriate number of partitions as you load data into your data warehouse to prevent [poor columnstore index quality](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-tables-index#causes-of-poor-columnstore-index-quality).

    * A row group is a chunk of rows that are compressed together in columnstore. To get full speed from your data warehouse, it is important to maximize columnstore row group quality. For best compression and index efficiency, the columnstore index needs to compress the maximum of 1,048,576 rows into each row group.

3. Reduce query data movement operations by [investigating your query plan](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-manage-monitor#monitor-query-execution). You can have a suboptimal plan with:

    * A poor selection of a table distribution key causing [data skew](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-tables-distribute#how-to-tell-if-your-distribution-column-is-a-good-choice)
    * Broadcast move operations which can be avoided by [replicating certain tables](https://docs.microsoft.com/azure/sql-data-warehouse/design-guidance-for-replicated-tables#convert-existing-round-robin-tables-to-replicated-tables)

4. Monitor to [ensure your query is not queued](https://docs.microsoft.com/azure/sql-data-warehouse/analyze-your-workload#queued-query-detection-and-other-dmvs) and your data warehouse has enough concurrency slots

    * SQL Data Warehouse has a fixed number of concurrency slots depending on the current service level. Queries require several concurrently slots based on their resource class to ensure adequate resources are provided for optimal and efficient query performance. They become queued when there are not enough [slots available](https://docs.microsoft.com/azure/sql-data-warehouse/memory-concurrency-limits).

5. Ensure [enough tempdb and memory have been allocated](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-manage-monitor#monitor-tempdb) during query execution

    * It is recommended to scale if you see your data warehouse is close to maxing out its tempdb capacity during high activity. Tempdb is used as a staging area for data movement operations as well as when a query reaches its memory grant.
    * Each query has a specific memory grant depending on its resource class and the data warehouse service level. When queries consume their grant, they must spill into tempdb slowing down query performance.

6. Avoid directly issuing queries against external tables by [loading data first](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-best-practices#load-then-query-external-tables):

    * External tables are not optimal for queries. External tables residing in Blob storage or Azure data lake does not have compute resources backing them; there the data warehouse cannot offload this work. Therefore, your data warehouse will be required to read the entire file into tempdb to scan the data.

7. Check [Analyze your workload in Azure Synapse Analytics](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/analyze-your-workload#queued-query-detection-and-other-dmvs) for queued query and the resources a request is waiting for
* Check [Sys.dm_pdw_errors](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-pdw-errors-transact-sql?view=azure-sqldw-latest) for errors
* If you experience slow query or load performance, ensure you have allocated enough memory. Check [Example code for finding the best resource class](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/resource-classes-for-workload-management#example-code-for-finding-the-best-resource-class).
* Internal DMS errors related to columnstore compression exceeding the remaining memory can be addressed by [increasing the resource class](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/resource-classes-for-workload-management#change-a-users-resource-class).

## **Recommended Documents**

* [Performance tuning with result set caching](https://docs.microsoft.com/azure/sql-data-warehouse/performance-tuning-result-set-caching)
* [Performance tuning with ordered clustered columnstore index](https://docs.microsoft.com/azure/sql-data-warehouse/performance-tuning-ordered-cci)
* [Performance tuning with materialized views](https://docs.microsoft.com/azure/sql-data-warehouse/performance-tuning-materialized-views)
* [Analyze your workload in Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/analyze-your-workload#queued-query-detection-and-other-dmvs)
* [Workload management with resource classes in Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/resource-classes-for-workload-management)


