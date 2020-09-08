<properties
	pageTitle="Resolve poor performance issues due to high IO utilization in Azure SQL Database"
	description="Resolve poor performance issues due to high IO utilization in Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
 	ms.author="andikshi"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32749516"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    	resourceTags="servers, databases"
	articleId="sql-performanceandqueryexecution-error10928-reqeustlimitforthedatabasereached"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve poor performance issues due to high IO utilization in Azure SQL Database

IO Usage is split into two types: Data IO and Log IO.Your can quickly identify the IO usage using the query below.
```
SELECT end_time, avg_data_io_percent, avg_log_write_percent
FROM sys.dm_db_resource_stats
ORDER BY end_time DESC;
```

If the IO usage is above 80% you have two options:

* Option 1: Upgrade the compute size or service tier
* Option 2: Identify and tune the queries consuming the most IO.

### **How To identify and top IO consuming queries**

When identifying IO performance issues, the top wait types associated with IO issues are:
* PAGEIOLATCH_*
For data file IO issues (including PAGEIOLATCH_SH, PAGEIOLATCH_EX, PAGEIOLATCH_UP). If the wait type name has IO in it, it points to an IO issue. If there is no IO in the page latch wait name, it points to a different type of problem (for example, tempdb contention).
* WRITE_LOG
For transaction log IO issues.

Use the [sys.dm_exec_requests](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-exec-requests-transact-sql?view=sql-server-ver15) or [sys.dm_os_waiting_tasks](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-os-waiting-tasks-transact-sql?view=sql-server-ver15) to see the wait_type and wait_time.

To identify the queries follow [IO Issues](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs#identify-io-performance-issues). 

## **Query Store**

The SQL Server [Query Store](https://docs.microsoft.com/sql/relational-databases/performance/monitoring-performance-by-using-the-query-store?redirectedfrom=MSDN&view=sql-server-ver15) feature provides you with insight on query plan choice and performance. It simplifies performance troubleshooting by helping you quickly find performance differences caused by query plan changes. Query Store automatically captures a history of queries, plans, and runtime statistics, and retains these for your review.
You can fetch the query ID's for TOP IO Consuming (Logical and physical reads) queries by slecting the paticular metic under the regressed queries section of the Query store.

## **Query performance insights**

[Query Performance Insight](https://docs.microsoft.com/azure/sql-database/sql-database-query-performance?WT.mc_id=pid:13491:sid:32630459/) provides intelligent query analysis for single and pooled databases. It helps identify the top resource consuming and long-running queries in your workload. This helps you find the queries to optimize to improve overall workload performance and efficiently use the resource that you are paying for.

## **Recommended Documents**

* Poor performance in Azure SQL DB is most often either related to excessive CPU utilization or a query waiting on a resource. To resolve either of these issues, review [Monitoring and performance tuning](https://docs.microsoft.com/azure/sql-database/sql-database-monitor-tune-overview?WT.mc_id=pid:13491:sid:32630450/).
* [IO Issues](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs#identify-io-performance-issues) 

