<properties
	pageTitle="performance and query execution/specific errors or exceptions"
	description="performance and query execution/specific errors or exceptions"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    ms.author="emlisa"
	displayOrder="6"
	selfHelpType="generic"
	supportTopicIds="326304540"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
	articleId="7d57d34f-58d4-4f40-99e2-0dc8e40ab2b4-new-st"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# performance and query execution/specific errors or exceptions

## **Recommended Documents**

Use [this reference](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues?WT.mc_id=pid:13491:sid:32745425/) to prevent, troubleshoot, diagnose, and mitigate connection errors and transient errors that your client application encounters when it interacts with Azure SQL Database. Information about specific SQL error codes for SQL Database client applications can be found [here](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages). Further information about specific database engine error messages can be found [here](https://docs.microsoft.com/sql/relational-databases/errors-events/database-engine-events-and-errors?view=sql-server-2017?WT.mc_id=pid:13491:sid:32745425/). Information about troubleshooting specific common errors is given below.  

### Error 9002: The transaction log for database X is full.

* Use [this reference](https://docs.microsoft.com/sql/relational-databases/logs/troubleshoot-a-full-transaction-log-sql-server-error-9002?view=sql-server-2017?WT.mc_id=pid:13491:sid:32745425/) to assist in troubleshooting a full transaction log. This will also provide suggestions on how to avoid this in the future. <br>

### Error 10928: The session limit for the database is X and has been reached

* The Resource ID indicates which resource governance limit is being hit. A value of 1 is a limit on worker threads; 2 is a limit on sessions (connections).  For short term mitigation, increase the [service tier](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-dtu?WT.mc_id=pid:13491:sid:32745425/) of your database; longer term, tune the workload so it better fits the selected tier. Refer to the [Query Performance Insight](https://docs.microsoft.com/azure/sql-database/sql-database-query-performance?WT.mc_id=pid:13491:sid:32745425/) feature for assistance analyzing and tuning your workload. <br>

### Error 701: There is insufficient system memory to run this query

* Use [this reference](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-701-database-engine-error?view=sql-server-2017?WT.mc_id=pid:13491:sid:32745425/) for assistance in troubleshooting this error. SQL Server has failed to allocate sufficient memory to run the query. This can be caused by a variety of reasons including operating system settings, physical memory availability, or memory limits on the current workload. In most cases, the transaction that failed is not the cause of this error. <br>

### Error 10930: The service is currently too busy

* Use [this reference](https://docs.microsoft.com/azure/expressroute/expressroute-troubleshooting-network-performance?WT.mc_id=pid:13491:sid:32745425/) to assist in standardizing a way to easily and consistently test network latency and bandwidth between two hosts as well as look at the Azure network to help isolate problem points. <br>

### Error 1205: Transaction (Process ID X) was deadlocked on Y

* Use [this reference](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-1205-database-engine-error?view=sql-server-2017?WT.mc_id=pid:13491:sid:32745425/) for assistance in troubleshooting this error. Resources are accessed in conflicting order on separate transactions, causing a deadlock. The system will detect this deadlock and will choose one of the transactions involved as a 'victim' and will issue this message, rolling back the victim's transaction. <br>

### Error 845: Time-out occurred while waiting for buffer latch type X for page Y, database ID Z.

* Use [this reference](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-845-database-engine-error?view=sql-server-2017?WT.mc_id=pid:13491:sid:32745425/) for assistance in troubleshooting this error. A process was waiting to acquire a latch, but the process waited until the time limit expired and failed to acquire one. This can occur if an I/O operation takes too long to complete, usually as a result of other tasks blocking system processes
