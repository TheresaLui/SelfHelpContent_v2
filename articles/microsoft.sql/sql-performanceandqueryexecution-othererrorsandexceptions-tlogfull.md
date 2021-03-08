<properties
	pageTitle="Resolve Full Transaction Log (SQL Server Error 9002)"
	description="Resolve Full Transaction Log (SQL Server Error 9002)"
	infoBubbleText="Resolve Full Transaction Log (SQL Server Error 9002)"
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
	articleId="eb872f6d-7dd9-46cc-8d8b-0b377647886b"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>

# Resolve Full Transaction Log (SQL Server Error 9002)

A very long-running transaction can cause the transaction log to fill. 

### Discovering long-running transactions

1. You can use Query performance Insight to identify the [Log Running Queries](button-data-blade:SqlAzureExtension.QueryPerformanceInsightBlade.databaseResourceId.$resourceId)

2. To look for long-running transactions, use the following:

[sys.dm_tran_database_transactions](https://docs.microsoft.com/sql/relational-databases/system-dynamic-management-views/sys-dm-tran-database-transactions-transact-sql?view=sql-server-ver15). This dynamic management view returns information about transactions at the database level. For a long-running transaction, columns of particular interest include the time of the first log record (database_transaction_begin_time), the current state of the transaction (database_transaction_state), and the log sequence number (LSN) of the begin record in the transaction log (database_transaction_begin_lsn).

[DBCC OPENTRAN](https://docs.microsoft.com/sql/t-sql/database-console-commands/dbcc-opentran-transact-sql?view=sql-server-ver15). This statement lets you identify the user ID of the owner of the transaction, so you can potentially track down the source of the transaction for a more orderly termination (committing it rather than rolling it back).

### Kill a transaction

Sometimes you just have to end the process; you may have to use the KILL statement. Please use this statement very carefully, especially when critical processes are running that you don't want to kill. For more information,see [KILL (Transact-SQL)](https://docs.microsoft.com/sql/t-sql/language-elements/kill-transact-sql?view=sql-server-ver15)

Other appropriate responses to a full transaction log depends partly on what condition or conditions caused the log to fill.
To discover what is preventing log truncation in a given case, use the log_reuse_wait and log_reuse_wait_desc columns of the [sys.database](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sys-databases-transact-sql?view=sql-server-ver15) catalog view. For more information, see sys.databases (Transact-SQL). For descriptions of factors that can delay log truncation, see [The Transaction Log (SQL Server)](https://docs.microsoft.com/sql/relational-databases/logs/the-transaction-log-sql-server?view=sql-server-ver15).

## **Recommended Documents**

Use [this reference](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues?WT.mc_id=pid:13491:sid:32630429/) to prevent, troubleshoot, diagnose, and mitigate connection errors and transient errors that your client application encounters when it interacts with Azure SQL Database. Information about specific SQL error codes for SQL Database client applications can be found [here](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages). Further information about specific database engine error messages can be found [here](https://docs.microsoft.com/sql/relational-databases/errors-events/database-engine-events-and-errors?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630429/). Information about troubleshooting specific common errors is given below.  

