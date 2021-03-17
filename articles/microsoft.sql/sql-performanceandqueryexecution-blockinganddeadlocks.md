<properties
	pageTitle="Blocking and deadlock issues with Azure SQL Database"
	description="Blocking and deadlock issues with Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  	ms.author="andikshi"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32749512"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    	resourceTags="servers, databases"
	articleId="sql-performanceandqueryexecution-blockinganddeadlocks"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve Blocking and deadlock issues with Azure SQL Database

### **Blocking**

Slow or long-running queries can contribute to excessive resource consumption and be the consequence of blocked queries; in other words, poor performance. While the concepts of blocking are the same for SQL Server and Azure SQL Database, the default isolation level is different. For Azure SQL Databases, **[READ_COMMITTED_SNAPSHOT](https://docs.microsoft.com/dotnet/framework/data/adonet/sql/snapshot-isolation-in-sql-server)** is enabled by default.

Blocking is an unavoidable characteristic of any relational database management system with lock-based concurrency. See [Understand and Resolve Azure SQL Database Blocking Problems](https://docs.microsoft.com/azure/azure-sql/database/understand-resolve-blocking) for more information on diagnosing and solving blocking issues. 

The following query will display the top ten running queries with the longest total elapsed time that are blocking other queries:

```
SELECT TOP 10 
	r.session_id,r.plan_handle,r.sql_handle,r.request_id,r.start_time, r.status,r.command, r.database_id,r.user_id, r.wait_type
	,r.wait_time,r.last_wait_type,r.wait_resource, r.total_elapsed_time,r.cpu_time, r.transaction_isolation_level,r.row_count,st.text 
FROM sys.dm_exec_requests r 
CROSS APPLY sys.dm_exec_sql_text(r.sql_handle) as st  
WHERE r.blocking_session_id = 0 and r.session_id in (SELECT distinct(blocking_session_id) FROM sys.dm_exec_requests) 
GROUP BY 
	r.session_id, r.plan_handle,r.sql_handle, r.request_id,r.start_time, r.status,r.command, r.database_id,r.user_id, r.wait_type
	,r.wait_time,r.last_wait_type,r.wait_resource, r.total_elapsed_time,r.cpu_time, r.transaction_isolation_level,r.row_count,st.text  
ORDER BY r.total_elapsed_time desc
```

### **Deadlock**

A deadlock occurs when two or more processes are waiting on the same resource, and each process is waiting on the other process to complete before moving forward.

This query can help you capture deadlock:

```
WITH CTE AS (
       SELECT CAST(event_data AS XML)  AS [target_data_XML] 
       FROM sys.fn_xe_telemetry_blob_target_read_file('dl', null, null, null)

)

SELECT 
    target_data_XML.value('(/event/@timestamp)[1]', 'DateTime2') AS Timestamp,
    target_data_XML.query('/event/data[@name=''xml_report'']/value/deadlock') AS deadlock_xml,
    target_data_XML.query('/event/data[@name=''database_name'']/value').value('(/value)[1]', 'nvarchar(100)') AS db_name
FROM CTE
```

To obtain a deadlock graph:

* Copy the `deadlock_xml` column results from the previous query and load into a text file. If more than one row is returned, you'll want to do each row result separately.
* Save the file as a `.xdl` extension, (for example, `deadlock.xdl`). This file can be viewed in tools such as SQL Server Management Studio as a deadlock report/graph.

If you need to customize the events you capture when a deadlock occurs, create your own [Extended Events](https://docs.microsoft.com/azure/azure-sql/database/xevent-db-diff-from-svr) Session with the following events for a deadlock.

* `Lock_Deadlock`: Occurs when an attempt to acquire a lock is canceled for the victim of a deadlock
* `Lock_deadlock_chain`: Occurs when an attempt to acquire a lock generates a deadlock. This event is raised for each participant in the deadlock.

## **Recommended Documents**

* [Understand and resolve blocking](https://docs.microsoft.com/azure/azure-sql/database/understand-resolve-blocking)
* [Find blocking queries](https://azure.microsoft.com/blog/finding-blocking-queries-in-sql-azure/)
* [Deadlocks](https://techcommunity.microsoft.com/t5/azure-database-support-blog/lesson-learned-19-how-to-obtain-the-deadlocks-of-your-azure-sql/ba-p/368847)
* [Locks](https://docs.microsoft.com/sql/relational-databases/sql-server-transaction-locking-and-row-versioning-guide?view=sql-server-ver15)
* [Monitoring and performance tuning](https://docs.microsoft.com/azure/azure-sql/database/monitor-tune-overview)
