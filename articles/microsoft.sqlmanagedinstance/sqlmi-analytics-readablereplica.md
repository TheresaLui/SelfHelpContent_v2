<properties
	pageTitle="Reporting Analytics Integration|Readable replica"
	description="Reporting Analytics Integration|Readable replica"
	service="microsoft.sql"
	resource="servers"
	authors="MladjoA"
    ms.author="mlandzic"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637298,32637297"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    articleId="fb72aa6e-19a3-4163-a1d9-30a217dfa064"
	ownershipId="AzureData_AzureSQLMI"
/>

# Readable replica

The Read Scale-Out feature in Business Critical service tier of Azure SQL Managed Instance allows you to load-balance read-only workloads using the capacity of one of the read-only replicas instead of sharing the capacity of primary replica. This way the read-only workload will be isolated from the main read-write workload and will not affect its performance.

## **Recommended Steps**

- Make sure that your SQL connection string is configured with `ApplicationIntent=ReadOnly` if you want to connect to readable replica
- Verify that you are connected to readable replica by executing command `SELECT DATABASEPROPERTYEX(DB_NAME(), 'Updateability')`
- When connected to a read-only replica, you can access the performance metrics using the `sys.dm_db_resource_stats` DMV
- To access query plan statistics, use the `sys.dm_exec_query_stats`, `sys.dm_exec_query_plan`, and `sys.dm_exec_sql_text` DMVs

## **Recommended Documents**

- [Use read-only replicas to load-balance read-only query workloads](https://docs.microsoft.com/azure/sql-database/sql-database-read-scale-out)
