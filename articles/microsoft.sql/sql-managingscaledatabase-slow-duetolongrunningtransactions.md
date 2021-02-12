<properties
	pageTitle="Scale database - slow due to long running transactions"
	description="Performance tier change is slow due to long running transactions"
	infoBubbleText="Found an ongoing scale issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="Anvesha4"
    ms.author="jterh,andikshi"
	displayOrder="16"
	articleId="UpdaSloKillLongRunningTransactions_A5D06371-7DA1-4999-B474-9B020FEB9071"
	diagnosticScenario="DiagnosticId.SqlProvision"
	selfHelpType="Diagnostics"
	supportTopicIds="32574333"
	resourceTags="servers, databases"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>
# We ran diagnostics on your resource and found an ongoing scale issue.

<!--issueDescription-->
You have initiated a scale operation on your Azure SQL DB database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> in server <!--$ServerName-->ServerName<!--/$ServerName-->. <br>
This operation is proceeding slowly due to long running transactions on the database.
<!--/issueDescription-->

Before the scale operation switches the database to the target performance tier, it ends any active transactions on the source instance to avoid long recovery on the target instance. Recovery is a database process that occurs when a database is restarted after a shutdown. Shutdown happens after the target instance starts up during a scale operation. Recovery rolls back all inflight but uncommitted transactions at the time of restart, and during this time the database is unavailable for additional requests. 

If there are any large transactions to rollback, this activity takes time proportional to the number of the active transactions. We recommend terminating any open transactions on your database to avoid long recovery of the target instance and speed up the scale operation. Please refer the links below for related information.

## **Recommended Steps**

Close any open transactions on your database to speed up the scale operation and avoid long recovery.

Use the [sys.dm_tran_active_transactions](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-tran-active-transactions-transact-sql?view=sql-server-ver15) DMV to view the open transactions. 

## **Recommended Documents**

* [SQL Transaction Log](https://docs.microsoft.com/sql/relational-databases/logs/the-transaction-log-sql-server)
* [Azure SQL scale single DB resources](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-scale)
* [Azure SQL scale elastic pool resources](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool-scale)
* [Azure SQL database DTU-based resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits/)
* [Azure SQL database vCore-based resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-vcore-resource-limits-single-databases/)
* To identify the top resource consuming and long-running queries in your workload use [Query Performance Insight](https://docs.microsoft.com/azure/azure-sql/database/query-performance-insight-use)
