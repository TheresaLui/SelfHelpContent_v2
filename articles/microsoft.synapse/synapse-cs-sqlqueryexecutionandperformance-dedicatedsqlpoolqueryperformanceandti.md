<properties
  pagetitle="SQL Query Execution and Performance/Dedicated SQL pool - Query performance and timeout&#xD;"
  description="SQL Query Execution and Performance/Dedicated SQL pool - Query performance and timeout"
  service="microsoft.synapse"
  resource="sqlpools"
  ms.author="saltug,goventur"
  selfhelptype="Generic"
  supporttopicids="32783869"
  resourcetags=""
  productpesids="15818"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="synapse-cs-sqlqueryexecutionandperformance-dedicatedsqlpoolqueryperformanceandti.md"
  ownershipid="AzureData_SynapseAnalytics" />
# SQL Query Execution and Performance/Dedicated SQL pool - Query performance and timeout

## **Recommended Steps**

**Following are the troubleshooting steps for the most common issues related to slow query performance:**

1. Use these [DMV queries](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-manage-monitor?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json) to troubleshoot waiting queries, tempdb, memory, transaction log, and Polybase load issues. Common causes include:
   * Long-running queries causing blocking.
   * A session leaves a transaction open holding locks, but is not actively running queries. This will block other queries.

2. Use the DMV queries from these articles to [troubleshoot resource classes](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/analyze-your-workload?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json) and [manage workloads](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-how-to-manage-and-monitor-workload-importance#monitor-importance).
Review the [memory and concurrency limits](https://docs.microsoft.com/azure/sql-data-warehouse/memory-concurrency-limits) and use [this sample query](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/resource-classes-for-workload-management#example-code-for-finding-the-best-resource-class) to find the optimal resource class.

3. Review recommendations from [Azure Advisor recommendations](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-concept-recommendations). For example, outdated statistics or data skew issues.

4. Analyze [cache metrics](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-how-to-monitor-cache?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json) for optimal usage based on cache hit ratio and space usage.

5. Query the DMV [sys.dm_pdw_errors](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-pdw-errors-transact-sql?view=azure-sqldw-latest) for errors.

6. Use Synapse Studio to [monitor SQL requests](https://docs.microsoft.com/azure/synapse-analytics/monitoring/how-to-monitor-sql-requests) and [SQL pools](https://docs.microsoft.com/azure/synapse-analytics/monitoring/how-to-monitor-sql-pools).

7. Review the [most common problems that lead to slow performance](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-troubleshoot#performance) and learn how to fix them.

8. Use Azure Monitor Logs to [investigate query execution and workload trends](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-monitor-workload-portal?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json) using log analytics.

9. Use Azure portal to [configure diagnostic settings](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-concept-resource-utilization-query-activity?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json) in order to analyze historic workload trends and query execution.

10. If your workload is still showing performance problems, your instance may have reached the performance limits for the current SLO. Learn [how to find the right DWU size](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-manage-compute-overview#finding-the-right-size-of-data-warehouse-units) for your workload.

**Recommendations and best practices for optimizing query performance:**

1. Troubleshooting query execution timeout errors:
    *  Check the timeout value that is configured on the client application.
    * Query execution timeout may be configured in workload groups to cancel queries that have exceeded the specified value. Check if the `QUERY_EXECUTION_TIMEOUT_SEC` parameter is configured in [`CREATE WORKLOAD GROUP`](https://docs.microsoft.com/sql/t-sql/statements/create-workload-group-transact-sql?toc=/azure/synapse-analytics/sql-data-warehouse/toc.json&bc=/azure/synapse-analytics/sql-data-warehouse/breadcrumb/toc.json&view=azure-sqldw-latest) syntax.

2. Statistics maintenance:
    * Statistics are created automatically by default, but not updated automatically. Learn how to [identify stale statistics](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-tables-statistics#update-statistics) and how to [keep statistics up-to-date](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-tables-statistics#implementing-statistics-management).
    * Statistics are not created automatically on temporary or external tables.
    * Statistics are created synchronously. Therefore, you may incur slightly degraded query performance if your columns are missing statistics.

3. Columnstore Index maintenance:
    * Learn how to [optimize clustered columnstore indexes](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-tables-index#optimizing-clustered-columnstore-indexes)/
    * Review the typical causes for [poor columnstore index quality](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-tables-index#causes-of-poor-columnstore-index-quality).
    * Use the larger resource classes to rebuild columnstore indexes for optimal memory allocation.

4. `Tempdb` management:
    * Use [this query](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-manage-monitor#monitor-tempdb) to monitor `tempdb` space used.
    * Typical consumers of `tempdb` space are `CREATE TABLE AS SELECT (CTAS)` or `INSERT SELECT` statements that fail in the final data movement operation. The most common mitigation is to break your `CTAS` or `INSERT SELECT` statement into multiple load statements, so that the data volume will not exceed the 1 TB per node `tempdb` limit.
    * Consider scaling your cluster to a larger size, which spreads the `tempdb` size across more nodes, reducing the `tempdb` on each individual node.
    * Complex queries running with insufficient memory can spill into `tempdb`, causing queries to fail. Consider running with a larger resource class to avoid spilling into `tempdb`.

5. Query data movement operations:
    * [Investigate your query plan](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-manage-monitor#monitor-query-execution).
    * A poor selection of a table distribution key can cause [data skew](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-tables-distribute#how-to-tell-if-your-distribution-column-is-a-good-choice).
    * Some Broadcast Move operations can be avoided by [replicating certain tables](https://docs.microsoft.com/azure/sql-data-warehouse/design-guidance-for-replicated-tables#convert-existing-round-robin-tables-to-replicated-tables).
    * Internal DMS errors related to columnstore compression exceeding the remaining memory can be addressed by [increasing the resource class](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/resource-classes-for-workload-management#change-a-users-resource-class).

6. Queries against external tables:
    * Avoid directly issuing queries against external tables by [loading data first](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-best-practices#load-then-query-external-tables).
    * External tables are not optimal for end user queries. Dedicated SQL pool will be required to read the entire file into `tempdb` first to scan the data.


## **Recommended Documents**

* [Performance tuning with result set caching](https://docs.microsoft.com/azure/sql-data-warehouse/performance-tuning-result-set-caching)

* [Performance tuning with ordered clustered columnstore index](https://docs.microsoft.com/azure/sql-data-warehouse/performance-tuning-ordered-cci)

* [Performance tuning with materialized views](https://docs.microsoft.com/azure/sql-data-warehouse/performance-tuning-materialized-views)

* [Analyze your workload in dedicated SQL pool](https://docs.microsoft.com/azure/sql-data-warehouse/analyze-your-workload#queued-query-detection-and-other-dmvs)

* [Workload management with resource classes in dedicated SQL pool](https://docs.microsoft.com/azure/sql-data-warehouse/resource-classes-for-workload-management)
