<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "sqlPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738820"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "SQL Performance and Query Execution/SQL pool query failure"
	description = "SQL Performance and Query Execution/SQL pool query failure"
	articleId = "synapse-sqlperformanceandqueryexecution-sqlpoolqueryfailure"
	authors = "saltug"
	ms.author = "saltug"
/>

# SQL Performance and Query Execution/SQL pool query failure

## **Recommended Steps**

* Check [Analyze your workload in Azure SQL Data Warehouse](https://docs.microsoft.com/azure/sql-data-warehouse/analyze-your-workload#queued-query-detection-and-other-dmvs) for queued query and the resources a request is waiting for
* To resolve out of memory errors, [try increasing the user's resource class](https://docs.microsoft.com/azure/sql-data-warehouse/resource-classes-for-workload-management#change-a-users-resource-class) or [scale your data warehouse to a larger service level](https://docs.microsoft.com/azure/sql-data-warehouse/quickstart-scale-compute-portal)
* To resolve syntax error for queries, check the [T-SQL syntax](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-reference-tsql-statements)
* To resolve, error: "Database 'Distribution_40_Cache' cannot be opened due to inaccessible files or insufficient memory or disk space", try pausing and resuming your data warehouse
* To resolve, error: "Unable to allocate ###### KB for columnstore compression because it exceeds the remaining memory from total allocated for current resource class and DWU" [try increasing the user's resource class](https://docs.microsoft.com/azure/sql-data-warehouse/resource-classes-for-workload-management#change-a-users-resource-class)

## **Recommended Documents**

* [Sys.dm_pdw_errors](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-pdw-errors-transact-sql?view=azure-sqldw-latest)
* [Additional Troubleshooting](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-troubleshoot/)


