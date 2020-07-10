<properties
	pageTitle="Performance and Query Execution/Query performance and timeouts"
	description="Performance and Query Execution/Query performance and timeouts"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
    ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637296"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="c4abfa00-1b0f-48cd-adc1-256665fb436b"
	ownershipId="AzureData_AzureSQLMI"
/>

# Query Performance troubleshooting

Azure SQL Database Managed Instance provides a set of the tools that enables you to easily troubleshoot and fix performance issues.

## **Recommended Steps**

Performance troubleshooting strategies vary depending on the class of the problem.

- If you have different workload performance on two different environments such as SQL Server and Managed Instance or two Managed Instances, try to identify the differences that can cause the issues
- If you see some queries that are running slower on Managed instance compared to the past executions, identify what caused the change in execution

## Different performance compared across two environments

If you are seeing that queries or workload don't have similar performance across two different environments try to identify what is the key differences using the following steps:

- Make sure that you have similar technical and environmental characteristics on SQL Server and Managed Instance such as number of cores, memory, IO characteristics, encryption, backup schedules, etc. Find the [top reasons that can cause performance difference in this article](https://azure.microsoft.com/blog/key-causes-of-performance-differences-between-sql-managed-instance-and-sql-server/).
- Make sure that you are following [the best practices for performance comparison](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/The-best-practices-for-performance-comparison-between-Azure-SQL/ba-p/683210)
- Look at the queries that are executing on your Managed Instance and identify some additional workload that is not running on SQL Server (for example frequent backups, data load, index maintenance actions)
- Identify the queries that are running slower on Managed Instance and compare their underlying SQL plans using SSMS
  - If the plans are different, identify what causes the difference. Try to update statistics or rebuild the indexes that might affect plan. Optionally try to change compatibility level, use legacy cardinality estimator or apply some query hints.
  - If the plans are the same, identify some limit that the slower plan is hitting by executing some of the troubleshooting steps described in the following section

## Performance issues on Managed Instance

If you are experiencing some issues with the queries that are running slower on Managed Instance, use the following steps to troubleshoot the issues:

- Try to find the changes in the resource utilization using the [SQL Server Management Studio(SSMS) Performance Dashboard](https://docs.microsoft.com/sql/relational-databases/performance/performance-dashboard), [sys.server_resource_stats](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sys-server-resource-stats-azure-sql-database?view=azuresqldb-current) and other [Dynamic Management Views(DMV)](https://docs.microsoft.com/azure/sql-database/sql-database-monitoring-with-dmvs). SSMS and DMVs enable you to identify top resource consuming queries that are using the critical resource. Once you identify the queries you can perform the following actions:
  - Tune the queries that affect performance by rewriting them, adding the indexes, updating statistics, etc
  - Increase the resources by adding more vCores or memory if you see some bottleneck

- Try to find some regressed queries using [SQL Server Management Studio/Query store](https://docs.microsoft.com/sql/relational-databases/performance/monitoring-performance-by-using-the-query-store?toc=%2Fazure%2Fsql-database%2Ftoc.json#Regressed), or [sys.dm_db_tuning_recommendations](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-db-tuning-recommendations-transact-sql). Regressed queries can be automatically corrected if you have enabled automatic tuning feature using **ALTER DATABASE current SET AUTOMATIC_TUNING ( FORCE_LAST_GOOD_PLAN = ON )**, or you can manually corrected them using [sp_force_plan](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-query-store-force-plan-transact-sql) procedure.
- [Analyze wait statistics](https://blogs.msdn.microsoft.com/sqlserverstorageengine/2019/03/05/analyzing-wait-statistics-on-managed-instance/) to see why the workload is waiting and identify the queries that are waiting
- [Measure IO performance](https://blogs.msdn.microsoft.com/sqlserverstorageengine/2019/03/04/measuring-file-io-performance-on-managed-instance-qpi/) on your instance (especially if you see dominant **PAGEIOLATCH** or **WRITELOG** wait statistics) to see are you hitting some IO storage limit. You might need to pre-allocate files to get [better IO performance](https://techcommunity.microsoft.com/t5/DataCAT/Storage-performance-best-practices-and-considerations-for-Azure/ba-p/305525).
- Bypass internal proxy and set `ProxyOverride` setting to `Redirect` when you are not using a public end-point with [Powershell](https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstance) or [Azure CLI](https://docs.microsoft.com/cli/azure/sql/mi#az-sql-mi-update). Make sure that your client application is in the same region as Managed Instance.

## **Recommended Documents**

- [Monitoring and performance tuning](https://docs.microsoft.com/azure/sql-database/sql-database-monitor-tune-overview)
- [Azure SQL Analytics(Preview)](https://docs.microsoft.com/azure/azure-monitor/insights/azure-sql?toc=%2Fazure%2Fsql-database%2Ftoc.json)
- [Top reasons that can cause performance difference](https://azure.microsoft.com/blog/key-causes-of-performance-differences-between-sql-managed-instance-and-sql-server/)
- [Migration to Managed Instance - best practices](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-migrate).
