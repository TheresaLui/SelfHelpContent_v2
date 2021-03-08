<properties
	pageTitle="Resolve query store related errors and exceptions"
	description="Resolve query store related errors and exceptions"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  	ms.author="andikshi"
	displayOrder="2"
	selfHelpType="diagnostics"
	supportTopicIds="32749519"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
	articleId="255dc14f-e922-41a3-a44b-cf3df7a86124"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve query store related errors and exceptions

### Enable Query Store

Use the ALTER DATABASE statement to enable the query store for a given database. For example:
```
ALTER DATABASE SET QUERY_STORE = ON (OPERATION_MODE = READ_WRITE);
```
Query Store cannot be enabled for the master or tempdb databases.

### Check Query Store Space Usage
To check current the Query Store size and limit execute the following statement in the user database.
```
SELECT current_storage_size_mb, max_storage_size_mb
FROM sys.database_query_store_options;
```
### Extend the storage for Query store (if it is full)
If the Query Store storage is full use the following statement to extend the storage.
```
ALTER DATABASE <database_name>
SET QUERY_STORE (MAX_STORAGE_SIZE_MB = <new_size>);
```
### Cleanup the Query Store

Query Store internal tables are created in the PRIMARY filegroup during database creation and that configuration cannot be changed later. If you are running out of space you might want to clear older Query Store data by using the following statement.
```
ALTER DATABASE <db_name> SET QUERY_STORE CLEAR;
```
## **Recommended Documents**

[Query Store Overview](https://docs.microsoft.com/sql/relational-databases/performance/monitoring-performance-by-using-the-query-store?view=sql-server-ver15)
