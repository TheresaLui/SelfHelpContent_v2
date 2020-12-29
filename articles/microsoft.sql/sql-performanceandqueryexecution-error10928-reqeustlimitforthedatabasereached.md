<properties
	pageTitle="Resolve request limit timeout issues in Azure SQL Database"
	description="Resolve request limit timeout issues in Azure SQL Database"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
  	ms.author="andikshi"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32749513"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
        resourceTags="servers, databases"
	articleId="sql-performanceandqueryexecution-error10928-reqeustlimitforthedatabasereached"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# The session limit for the database has been reached

**Error 10928: Resource ID : 1: The worker limit for the database has been reached**

Sessions refer to the number of concurrent connections allowed to a SQL database at a time. Workers can be thought of as the processes in the SQL database that are processing queries. The maximum number of workers allowed depends on your databases' service tier.

Azure SQL DB limits the number of [concurrent workers](https://docs.microsoft.com/azure/azure-sql/database/resource-limits-dtu-single-databases?WT.mc_id=pid:13491:sid:32745427) allowed to the database. 

Use the [sys.dm_db_resource_stats](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-db-resource-stats-azure-sql-database?view=azuresqldb-current), to quickly check **Maximum concurrent workers (requests)** as a percentage of the limit of the database's service tier.
When the worker limit is reached, clients will receive an error message (Error 10928: Resource ID : 1) and will be unable to query your database.

## **Recommended Steps**

For an immediate solution, scale your database to a larger service tier sufficient to handle the workload.

Longer-term, you should:

* Optimize queries to reduce the resource utilization of each query if the cause of increased worker utilization is due to contention for compute resources. For more information, see [Query Tuning/Hinting](https://docs.microsoft.com/azure/azure-sql/database/performance-guidance#query-tuning-and-hinting).
* Reduce the [MAXDOP](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-the-max-degree-of-parallelism-server-configuration-option?view=sql-server-ver15#Guidelines) (maximum degree of parallelism) setting
* Optimize query workload to reduce number of occurrences and duration of query blocking

## **Recommended Documents**

* [Resource limits for single databases using the vCore purchasing model](https://docs.microsoft.com/azure/azure-sql/database/resource-limits-vcore-single-databases?WT.mc_id=pid:13491:sid:32745427)
