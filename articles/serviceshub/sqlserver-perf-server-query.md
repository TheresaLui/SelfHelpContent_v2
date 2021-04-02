<properties
 pageTitle="Troubleshooting SQL Server Performance issues"
 description="Troubleshooting SQL Server Performance issues"
 articleId="2457ee97-4273-4f0e-948c-21851c090509"
 productFamilyId = "7aa8b5ba-4d1a-644d-aeca-bc4decdb15de"
 productPesIds="16907,16899,16893,16887,16881"
 supportTopicIds="32684375,32684379"
 ms.author="ramakoni"
 ownershipId="serviceshub"
 selfHelpType="generic"
 cloudEnvironments="public, fairfax, usnat, ussec"
/>

# Troubleshooting SQL Server Performance issues

Most users are able to resolve their slow performance issues with SQL Server using the recommended methodology below.

## **Recommended Steps**

### Slow Performance Troubleshooting Methodology

1. **Find Slow Queries:** To establish if there are performance issues on your SQL Server, start by examining queries by their execution time (elapsed time). Check if that time that exceeds a threshold you have set (in milliseconds) based on a established baseline performance. For example, for your workload the threshold may be set for queries that run longer than 300 ms. You can identify all queries that exceed that threshold and then focus on each individual query and its pre-established performance baseline duration. Ultimately, business users care about the execution duration of their database queries and therefore the focus is on execution duration.

   This is an example of how to check for **currently-executing** queries beyond a predefined threshold:

   ```SQL
   SELECT    er.session_id,
             st.text batch_text,
             substring(st.text, (er.statement_start_offset/2),
             ((CASE er.statement_end_offset
                         WHEN -1 THEN datalength(st.text)
                         ELSE er.statement_end_offset
             END - er.statement_start_offset)/2) + 1) AS current_statement_text,
             er.total_elapsed_time,
             er.wait_time,
             er.cpu_time,
             er.logical_reads,
             er.writes
   FROM        sys.dm_exec_requests              AS er
   CROSS apply sys.dm_exec_sql_text (sql_handle) AS st
   WHERE er.total_elapsed_time > 300
   ORDER BY    er.total_elapsed_time DESC
   ```

   The following statement is an example of how to identify **historical queries** that took longer than you pre-defined threshold. This data returned is available for queries whose plans are still cached in plan cache.

   ```sql
   SELECT t.text,
       (qs.total_elapsed_time/1000) / qs.execution_count   as    avg_elapsed_time,
       (qs.total_worker_time/1000) / qs.execution_count    as    avg_cpu_time,
       qs.total_logical_reads / qs.execution_count  as    avg_logical_reads,
       qs.total_logical_writes / qs.execution_count as    avg_writes,
       (qs.total_elapsed_time/1000)                      as    cumulative_elapsed_time_all_executions
   FROM   sys.dm_exec_query_stats qs
       CROSS apply sys.Dm_exec_sql_text (sql_handle) t
   ORDER  BY (qs.total_elapsed_time / qs.execution_count) DESC
   ```

1. **Running vs. Waiting: Why are queries slow?** If you find queries that exceed your predefined threshold, next examine why they could be slow. The cause of performance problems can be grouped into two categories: RUNNING or WAITING

- WAITING: Queries can be slow because they are waiting on a bottleneck for a long time (see types of [Waits](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-os-wait-stats-transact-sql))
- RUNNING: Queries can be slow because they are running (executing) for a long time. This means these queries are actively using CPU resources.

  A query can be running for some time and waiting for some time in its lifetime (duration), but you want to establish which is the dominant category that contributes to its long elapsed time. Therefore, the first task is to establish in which category the queries fall. It is simple: if a query is not running, then it is waiting. Ideally, a query spends most of its elapsed time in running state and spend very little time waiting for resources. Also, in the best-case scenario a query runs within or below a predetermined baseline.

  **Diagnose and Resolve Waiting Queries:**

  To identify queries that are waiting on bottlenecks, you need to discover how long the waits are and what the bottleneck is ([wait types](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-os-wait-stats-transact-sql)). Once you identify the wait type, your goal is to reduced it or eliminate it completely.

  The wait time is roughly calculated by subtracting the cpu time (worker time) from the elapsed time of a query. The CPU time is actual execution time, the remaining part of the lifetime of the query is waiting.

- Here is a query to help identify historical long-waiting queries (>20% of overall elapsed time).

  ```sql
  SELECT t.text,
          qs.total_elapsed_time / qs.execution_count
          avg_elapsed_time,
          qs.total_worker_time / qs.execution_count
          avg_cpu_time,
          ( qs.total_elapsed_time - qs.total_worker_time ) / qs.   execution_count AS
          avg_wait_time,
          qs.total_logical_reads / qs.execution_count
          avg_logical_reads,
          qs.total_logical_writes / qs.execution_count
          avg_writes,
          qs.total_elapsed_time
          cumulative_elapsed_time
  FROM   sys.dm_exec_query_stats qs
          CROSS apply sys.Dm_exec_sql_text (sql_handle) t
  WHERE  ( qs.total_elapsed_time - qs.total_worker_time ) / qs.   total_elapsed_time  > 0.2
  ORDER  BY qs.total_elapsed_time / qs.execution_count DESC
  ```

- Also consider using [PerfStat script](https://github.com/microsoft/DiagManager/blob/master/DiagManager/CustomDiagnostics/SQL%20Server%20Perf%20Stats/SQL%20Server%20Perf%20Stats.sql) to identify waiting queries on your SQL Server instance over time.

- You can also gather wait statistics on your server (not specific to queries) by using this query

  ```sql
  DECLARE @logtime DATETIME
  SET @logtime = Getdate ()
  SELECT @logtime logtime, *
  INTO #wait_stats
  FROM sys.dm_os_wait_stats

  WAITFOR DELAY '00:05:00' --wait for 5 min and then capture another    snapshot so that you can compare

  SET @logtime = Getdate()

  INSERT INTO #wait_stats
  SELECT @logtime, *
  FROM   sys.dm_os_wait_stats
  ```

Once you have the above information in the _#wait_stats_ temp table, you can query it like this:

```SQL
SELECT wait_type,
       ( Max(wait_time_ms) - Min(wait_time_ms) ) / 60000 DeltaMin,
       Datediff(minute, Min(logtime), Max(logtime))      AS
       CollectionPeriodForThisWaitType,
       ( Max(wait_time_ms) - Min(wait_time_ms) ) / 600.00 /
       Datediff(minute, Min(logtime), Max(logtime))      AS
       PercentOfCollectionTIme
FROM   #wait_stats
GROUP  BY wait_type
ORDER  BY deltamin DESC
```

**_Common Bottleneck (Wait Types):_**

- Blocking (lock waits)
  - [Understaning Locking](https://docs.microsoft.com/sql/relational-databases/sql-server-transaction-locking-and-row-versioning-guide#Lock_Engine)
  - [Understanding and Resolving Blocking issues](https://docs.microsoft.com/troubleshoot/sql/performance/understand-resolve-blocking)
- Disk I/O waits
  - [identify I/O issues](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs#identify-io-performance-issues)
  - [Slow I/O and SQL Server - troubleshooting methodology](https://techcommunity.microsoft.com/t5/sql-server-support/slow-i-o-sql-server-and-disk-i-o-performance/ba-p/333983)
- Latch Waits
  - [resolve PAGELATCH_EX contention](https://support.microsoft.com/help/4460004/how-to-resolve-last-page-insert-pagelatch-ex-contention-in-sql-server)
- Memory Grant waits
  - [identify memory grant issues](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs#identify-memory-grant-wait-performance-issues)
  - [Memory grants explanation and solutons](https://techcommunity.microsoft.com/t5/sql-server-support/memory-grants-meditation-the-mysterious-sql-server-memory/ba-p/333994)
- Network I/O waits
- Log Write Waits

**Diagnose and Resolve Running Queries:**

When CPU (worker) time is very close to overall elapsed duration, then the query spent most of its lifetime executing. Typically when SQL Server engine is reported to drive high CPU, it is high-CPU queries that drive a large number of logical reads, that are the root cause. You can find queries that are mostly running, by using this historical DMV diagnostic.

```sql
SELECT t.text,
       qs.total_elapsed_time / qs.execution_count as avg_elapsed_time,
       qs.total_worker_time / qs.execution_count as avg_cpu_time,
       ( qs.total_elapsed_time - qs.total_worker_time ) / qs.execution_count AS avg_wait_time,
       qs.total_logical_reads / qs.execution_count as avg_logical_reads,
       qs.total_logical_writes / qs.execution_count as avg_writes,
       qs.total_elapsed_time as cumulative_elapsed_time
FROM   sys.dm_exec_query_stats qs
       CROSS apply sys.Dm_exec_sql_text (sql_handle) t
WHERE  ( qs.total_elapsed_time - qs.total_worker_time ) / qs.total_elapsed_time < 0.2
ORDER  BY qs.total_elapsed_time / qs.execution_count
```

**_Common Methods to Resolve Long-Running, CPU-bound Queries_**

- [Examine the query plan of the query ](https://docs.microsoft.com/sql/relational-databases/performance/display-an-actual-execution-plan)
- [Update Statistics](https://docs.microsoft.com/sql/t-sql/statements/update-statistics-transact-sql#examples)
- Identify and apply [Missing Indexes](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-db-missing-index-details-transact-sql). [This script](https://github.com/microsoft/DiagManager/blob/master/DiagManager/CustomDiagnostics/SQL%20Server%20Perf%20Stats/SQL%20Server%20Perf%20Stats%20Snapshot.sql) will help identify missing indexes
- Re-design or re-write the query(s)
- Identify and resolve [parameter-sensitive plans](https://docs.microsoft.com/azure/azure-sql/identify-query-performance-issues#ParamSniffing)
- [Assess and resolve cardinality estimation issues](https://docs.microsoft.com/sql/relational-databases/performance/cardinality-estimation-sql-server)
- [Identify CPU performance issues](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs#identify-cpu-performance-issues)
- Increase computing resources on the system (CPUs)

## **Recommended Documents**

- [Resolving queries with suboptimal query execution plans](https://docs.microsoft.com/azure/azure-sql/identify-query-performance-issues#ParamSniffing)

- [Performance Monitoring and Tuning Tools](https://docs.microsoft.com/sql/relational-databases/performance/performance-monitoring-and-tuning-tools)

- [Auto-Tuning Options in SQL Server](https://docs.microsoft.com/sql/relational-databases/automatic-tuning/automatic-tuning)

- [Index architecture and Design Guidelines](https://docs.microsoft.com/sql/relational-databases/sql-server-index-design-guide#General_Design)
