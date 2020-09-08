<properties
	pageTitle="Resolve questions or issues realted to space for Azure SQL Database"
	description="Resolve questions or issues realted to space for Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  	ms.author="andikshi"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32749518"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    	resourceTags="servers, databases"
	articleId="sql-performanceandqueryexecution-managingspacefordatabasesandpools"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve questions or issues realted to space for Azure SQL Database

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

The top wait types associated with tempdb issues is PAGELATCH_* (not PAGEIOLATCH_*). However, PAGELATCH_* waits do not always mean you have tempdb contention. This wait may also mean that you have user-object data page contention due to concurrent requests targeting the same data page. To further confirm tempdb contention, use [sys.dm_exec_requests](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-exec-requests-transact-sql?view=sql-server-ver15) to confirm that the wait_resource value begins with 2:x:y where 2 is tempdb is the database ID, x is the file ID, and y is the page ID.

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

If you are facing issues due to Tempdb being full, and are not able to resolve it, you can do a failover to clear tempdb. 
Failover changes the node of a database and moves it to a new node, it is recommended that you do not have any active workload running if you are doing a failover. 

<a href="https://docs.microsoft.com/rest/api/sql/databases(failover)/failover">Failover Rest API</a> can be used to easily failover your Azure SQL database to a new node.

## **Recommended Documents**

* For further details follow [TroubleshootTempDB issues](https://docs.microsoft.com/azure/azure-sql/database/monitoring-with-dmvs#identify-tempdb-performance-issues).

