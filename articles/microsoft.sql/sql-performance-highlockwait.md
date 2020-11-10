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

# High Lock Waits Detected

<!--issueDescription-->
We ran diagnostics and detected that your database **<!--$DatabaseName-->DatabaseName<!--/$DatabaseName-->** on server **<!--$ServerName-->ServerName<!--/$ServerName-->** is experiencing high wait times due to locking. Between **<!--$StartTime-->StartTime<!--/$StartTime-->** and **<!--$EndTime-->EndTime<!--/$EndTime-->**, we detected over ten 15-minute intervals with average lock times of more than 60 seconds.
<!--/issueDescription-->

## **Recommended Steps**

This high locking wait event is potentially contributing to performance issues. Blocking can occur due to lock wait times. Blocking occurs when one connection holds a lock on a specific resource and a second connection attempts to acquire a conflicting lock type on the same resource. The duration and transaction context of a query determine how long its locks are held and, thereby, their impact on other queries. 

To improve performance, follow these steps:
1. Identify which type of locks have the longest waits.
2. [Identify which queries may be blocking.](https://azure.microsoft.com/blog/finding-blocking-queries-in-sql-azure)
3. Verify the isolation levels and determine whether there are any locking hints used.
4. Tune the blocking queries and adjust transaction size and durationw where possible.

## **Recommended Documents**

* [Locking in the Database Engine](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/ms190615(v=sql.105)?redirectedfrom=MSDN)

