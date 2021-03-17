<properties
	pageTitle="Resolve questions or issues related to space for Azure SQL Database Managed Instance"
	description="Resolve questions or issues related to space for Azure SQL Database Managed Instance"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  	ms.author="andikshi"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32748870"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
	articleId="sqlmi-performanceandqueryexecution-managingspacefordatabasesandpools"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve questions or issues related to space for Azure SQL Database Managed Instance

### **Fastest way to mitigate low or no free space available**

* Increase storage, if service tier allows it
* Upgrade to a service tier that can provide more storage
* If you are facing issues due to Tempdb being full, you can do a failover to clear tempdb 

The [Failover Rest API](https://docs.microsoft.com/rest/api/sql/managed%20instances%20-%20failover/failover) can be used to easily failover your Azure SQL Managed Instance to a new node, which clears tempdb.  Note that existing connections will be dropped during the failover, so applications should handle the disconnect with appropriate retry logic.

### **Calculating database and objects sizes**

The following query returns the size of your database (in megabytes):

```
-- Calculates the size of the database.
SELECT SUM(CAST(FILEPROPERTY(name, 'SpaceUsed') AS bigint) * 8192.) / 1024 / 1024 AS DatabaseSizeInMB
FROM sys.database_files
WHERE type_desc = 'ROWS';
GO
```

The following query returns the size of individual objects (in megabytes) in your database:

```
-- Calculates the size of individual database objects.
SELECT sys.objects.name, SUM(reserved_page_count) * 8.0 / 1024
FROM sys.dm_db_partition_stats, sys.objects
WHERE sys.dm_db_partition_stats.object_id = sys.objects.object_id
GROUP BY sys.objects.name;
GO
```

### **TempDB Issues**

The top wait types associated with tempdb issues are PAGELATCH_* (not PAGEIOLATCH_*). However, PAGELATCH_* waits do not always mean you have tempdb contention. This wait may also mean that you have user-object data page contention due to concurrent requests targeting the same data page. 

To further confirm tempdb contention, use [sys.dm_exec_requests](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-exec-requests-transact-sql?view=sql-server-ver15) to confirm that the wait_resource value begins with 2:x:y where 2 is tempdb database ID, x is the file ID, and y is the page ID.  
For example: Wait Resource 2:1:3 is  
DatabaseID: 2 (TempDB)   
File Number: 1 (The first data file)   
Page Number: 3 (SGAM Page) )

For tempdb contention, a common method is to reduce or re-write application code that relies on tempdb. Common tempdb usage areas include:

* Temp tables
* Table variables
* Table-valued parameters
* Version store usage (specifically associated with long running transactions)
* Queries that have query plans that use sorts, hash joins, and spools

You can use the following query to identify top queries that use table variables and temporary tables:

```
SELECT plan_handle, execution_count, query_plan
INTO #tmpPlan
FROM sys.dm_exec_query_stats
     CROSS APPLY sys.dm_exec_query_plan(plan_handle);
GO

WITH XMLNAMESPACES('http://schemas.microsoft.com/sqlserver/2004/07/showplan' AS sp)
SELECT plan_handle, stmt.stmt_details.value('@Database', 'varchar(max)') 'Database', stmt.stmt_details.value('@Schema', 'varchar(max)') 'Schema', stmt.stmt_details.value('@Table', 'varchar(max)') 'table'
INTO #tmp2
FROM(SELECT CAST(query_plan AS XML) sqlplan, plan_handle FROM #tmpPlan) AS p
    CROSS APPLY sqlplan.nodes('//sp:Object') AS stmt(stmt_details);
GO

SELECT t.plan_handle, [Database], [Schema], [table], execution_count
FROM(SELECT DISTINCT plan_handle, [Database], [Schema], [table]
     FROM #tmp2
     WHERE [table] LIKE '%@%' OR [table] LIKE '%#%') AS t
    JOIN #tmpPlan AS t2 ON t.plan_handle=t2.plan_handle;
```

### **Long term mitigations**

* Analyze if column data types are the right ones for the data they will store
* Test compressing tables and/or indexes
* Depending on the workload and service tier, test [Columnstore indexes]( https://docs.microsoft.com/sql/relational-databases/indexes/columnstore-indexes-overview?view=sql-server-ver15)
* If possible export and remove data that is not needed or move to another database, with lower service tier, if the access pattern is low

### **Compression**
The [data compression]( https://docs.microsoft.com/sql/relational-databases/data-compression/data-compression?view=sql-server-ver15) feature help's to reduce the size of the database. In addition to saving space, data compression can help improve performance of I/O intensive workloads because the data is stored in fewer pages and queries need to read fewer pages from disk. However, extra CPU resources are required on the database server to compress and decompress the data, while data is exchanged with the application.

### **Alerts**
Several maintenance and administrative actions performed in a database require some storage for temporary data and for this reason it’s not recommended to allow the storage usage of the database to be very close to the its limits. To prevent your database to be very close to the storage limit is advised to implement [alerts](https://docs.microsoft.com/azure/azure-sql/managed-instance/alerts-create) or having other ways to monitor the storage usage.

## **Recommended Documents**

* [Troubleshoot TempDB issues](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs#identify-tempdb-performance-issues)
* [Enable Compression on a Table or Index](https://docs.microsoft.com/sql/relational-databases/data-compression/enable-compression-on-a-table-or-index?view=sql-server-ver15)

