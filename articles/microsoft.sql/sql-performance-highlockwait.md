<properties
    pageTitle="query execution/high locking waits"
    description="query execution/high locking waits"
    infoBubbleText="Detected high lock waits. See details on the right."
    service="microsoft.sql"
    resource="servers"
    authors="ketho00"
    ms.author="ketho"
    displayOrder=""
    articleId="LockWait_E35B0A66-E692-4508-899C-C1C0E5BBB131"
    diagnosticScenario="SqlPerfTsg"
    selfHelpType="diagnostics"
    supportTopicIds="32749512,32749514,32749515,32749520"
    resourceTags=""
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# High Locking Waits Detected - Performance Impacting
<!--issueDescription-->
We ran diagnostics and detected that your database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->** is experiencing high wait times due to locking. This is potentially contributing to performance issues. Between **<!--$StartTime-->StartTime<!--/$StartTime-->** and **<!--$EndTime-->EndTime<!--/$EndTime-->**, we detected over ten 15-minute intervals with average lock times of more than 60 seconds.
<!--/issueDescription-->

## **Recommended Steps**

To reduce locking waits and improve database performance, follow these recommendations:
* [Identify which type of locks have the longest waits](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-db-wait-stats-azure-sql-database?view=azuresqldb-current)
* [Identify blocking queries](https://azure.microsoft.com/blog/finding-blocking-queries-in-sql-azure/) and [tune blocking queries](https://docs.microsoft.com/azure/azure-sql/database/performance-guidance#tune-your-database)
* [Reduce transaction size and duration](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/ms175523%28v=sql.105%29)
* [Adjust or revert any snapshot isolation levels configured on your database](https://docs.microsoft.com/dotnet/framework/data/adonet/sql/snapshot-isolation-in-sql-server)
* [Adjust or revert any locking hints specified by your queries](https://docs.microsoft.com/sql/t-sql/queries/hints-transact-sql?view=sql-server-ver15)

## **Recommended Documents**

* [Locking in the Database Engine](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/ms190615%28v=sql.105%29)
* [Transaction Locking and Row Versioning Guide](https://docs.microsoft.com/sql/relational-databases/sql-server-transaction-locking-and-row-versioning-guide?view=sql-server-ver15)

