<properties
	pageTitle="Resolve tempDB related errors and exceptions"
	description="Resolve tempDB related errors and exceptions"
	infoBubbleText="Resolve tempDB related errors and exceptions"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  	ms.author="andikshi"
	displayOrder="1"
	selfHelpType="diagnostics"
	supportTopicIds="32749519"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
	articleId="ebc55c88-a4f5-4cb4-829d-35e6e165e490"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve tempDB related errors and exceptions

### TempDB Space Monitoring

The maximum space for each DB or Pool will depend on SLO for the database. You can find the various limits here:

* [DTU Model](https://docs.microsoft.com/sql/relational-databases/databases/tempdb-database?view=sql-server-ver15#tempdb-database-in-sql-database)
* [VCore Model](https://docs.microsoft.com/azure/azure-sql/database/resource-limits-vcore-single-databases)

You can monitor the Space Used/Free using the TSQL below:

```
-- Determining the Amount of Space Used  / free
SELECT 
	 [Source] = 'database_files'
	,[TEMPDB_max_size_MB] = SUM(max_size) * 8 / 1027.0
	,[TEMPDB_current_size_MB] = SUM(size) * 8 / 1027.0
	,[FileCount] = COUNT(FILE_ID)
FROM tempdb.sys.database_files
WHERE type = 0 --ROWS

SELECT 
	 [Source] = 'dm_db_file_space_usage'
	,[free_space_MB] = SUM(U.unallocated_extent_page_count) * 8 / 1024.0
	,[used_space_MB] = SUM(U.internal_object_reserved_page_count + U.user_object_reserved_page_count + U.version_store_reserved_page_count) * 8 / 1024.0
    ,[internal_object_space_MB] = SUM(U.internal_object_reserved_page_count) * 8 / 1024.0
    ,[user_object_space_MB] = SUM(U.user_object_reserved_page_count) * 8 / 1024.0
    ,[version_store_space_MB] = SUM(U.version_store_reserved_page_count) * 8 / 1024.0
FROM tempdb.sys.dm_db_file_space_usage U

-- Obtaining the space consumed currently in each session
SELECT 
	 [Source] = 'dm_db_session_space_usage'
	,[session_id] = Su.session_id
	,[login_name] = MAX(S.login_name)
	,[database_id] = MAX(S.database_id)
	,[database_name] = MAX(D.name)
	,[elastic_pool_name] = MAX(DSO.elastic_pool_name)
	,[internal_objects_alloc_page_count_MB] = SUM(internal_objects_alloc_page_count) * 8 / 1024.0
	,[user_objects_alloc_page_count_MB] = SUM(user_objects_alloc_page_count) * 8 / 1024.0
FROM tempdb.sys.dm_db_session_space_usage SU
LEFT JOIN sys.dm_exec_sessions S
        ON SU.session_id = S.session_id
LEFT JOIN sys.database_service_objectives DSO
        ON S.database_id = DSO.database_id
LEFT JOIN sys.databases D
	ON S.database_id = D.database_id
WHERE internal_objects_alloc_page_count + user_objects_alloc_page_count > 0
GROUP BY Su.session_id
ORDER BY [user_objects_alloc_page_count_MB] desc, Su.session_id;


-- Obtaining the space consumed in all currently running tasks in each session
SELECT 
	 [Source] = 'dm_db_task_space_usage'
	,[session_id] = SU.session_id
	,[login_name] = MAX(S.login_name)
	,[database_id] = MAX(S.database_id)
	,[database_name] = MAX(D.name)
	,[elastic_pool_name] = MAX(DSO.elastic_pool_name)
	,[internal_objects_alloc_page_count_MB] = SUM(SU.internal_objects_alloc_page_count) * 8 / 1024.0
	,[user_objects_alloc_page_count_MB] = SUM(SU.user_objects_alloc_page_count) * 8 / 1024.0
FROM tempdb.sys.dm_db_task_space_usage SU
LEFT JOIN sys.dm_exec_sessions S
        ON SU.session_id = S.session_id
LEFT JOIN sys.database_service_objectives DSO
        ON S.database_id = DSO.database_id
LEFT JOIN sys.databases D
	ON S.database_id = D.database_id
WHERE internal_objects_alloc_page_count + user_objects_alloc_page_count > 0
GROUP BY SU.session_id
ORDER BY [user_objects_alloc_page_count_MB] desc, session_id;
```
You can also connect directly to user DB and check if there is any session ID that have a open transaction using TEMPDB.

```
SELECT 
	 [Source] = 'database_transactions'
	,[session_id] = ST.session_id
	,[transaction_id] = ST.transaction_id
	,[database_id] = DT.database_id
	,[database_name] = CASE
		WHEN D.name IS NULL AND DT.database_id = 2 THEN 'TEMPDB'
		ELSE D.name
	 END
	,[database_transaction_log_used_Kb] = CONVERT(numeric(18,2), DT.database_transaction_log_bytes_used / 1024.0 )
	,[database_transaction_begin_time] = DT.database_transaction_begin_time
	,[transaction_type_desc] = CASE database_transaction_type
		WHEN 1 THEN 'Read/write transaction'
		WHEN 2 THEN 'Read-only transaction'
		WHEN 3 THEN 'System transaction'
		WHEN 4 THEN 'Distributed transaction'
	END
	,[transaction_state_desc] = CASE database_transaction_state
		WHEN 0 THEN 'The transaction has not been completely initialized yet'
		WHEN 1 THEN 'The transaction has been initialized but has not started'
		WHEN 2 THEN 'The transaction is active'
		WHEN 3 THEN 'The transaction has ended. This is used for read-only transactions'
		WHEN 4 THEN 'The commit process has been initiated on the distributed transaction. This is for distributed transactions only. The distributed transaction is still active but further processing cannot take place'
		WHEN 5 THEN 'The transaction is in a prepared state and waiting resolution.'
		WHEN 6 THEN 'The transaction has been committed'
		WHEN 7 THEN 'The transaction is being rolled back'
		WHEN 8 THEN 'The transaction has been rolled back'
	END
FROM sys.dm_tran_database_transactions DT
INNER JOIN sys.dm_tran_session_transactions ST
	ON DT.transaction_id = ST.transaction_id
LEFT JOIN sys.databases D
	ON DT.database_id = D.database_id
ORDER BY ST.session_id
```

### Global Temporary Tables

Azure SQL Database single databases and elastic pools support global temporary tables and global temporary stored procedures that are stored in tempdb and are scoped to the database level. Global temporary tables and global temporary stored procedures are shared for all users' sessions within the same Azure SQL database. User sessions from other Azure SQL databases cannot access [global temporary tables](https://docs.microsoft.com/sql/t-sql/statements/create-table-transact-sql?view=sql-server-ver15#database-scoped-global-temporary-tables-azure-sql-database)

## **Recommended Documents**

[Tempdb Database](https://docs.microsoft.com/sql/relational-databases/databases/tempdb-database?view=sql-server-ver15)

