<properties
	pageTitle="Managed Instance - Log nearly full"
	description="Managed Instance - Log nearly full"
	infoBubbleText="Managed Instance log file on some of the databases was getting close to its limits. See details on the right."
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="zlradeti"
	authors="zlradeti"
	displayOrder=""
	diagnosticScenario="SqlMIPerf_Log Nearly Full"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="sqlmanagedinstance-perf-log-near-full"
	ownershipId="AzureData_AzureSQLMI"
/>

# Managed Instance - Log nearly full

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named <!--$ServerName-->ServerName<!--/$ServerName--> on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> was facing a potential problem between <!--$startTime-->startTime<!--/$startTime--> and <!--$endTime-->endTime<!--/$endTime--> where some of the databases had its log file nearly full.

When the transaction log becomes full, SQL Server Database Engine issues a 9002 error. If the log fills while the database is online, the database remains online but can only be read, not updated. 

<!--/issueDescription-->

## **Recommended Steps**

- There are multiple reasons why log can get full and recommended actions strongly depend on the type of the issue which caused the log file getting full. Because of this, please check the following list of the affected databases and the issues noticed on them, and then continue with recommended steps depending on the type of the issue that database was facing.

  

  Affected databases:  <!--$AffectedDatabases-->AffectedDatabases<!--/$AffectedDatabases-->

  Auto-growth turned off:  <!--$AutoGrowthIssue-->AutoGrowthIssue<!--/$AutoGrowthIssue-->

  Instance storage limit hit: <!--$DiskFullIssue-->DiskFullIssue<!--/$DiskFullIssue-->

  Log file size misconfigured : <!--$LogSizeMisconfiguredIssue-->LogSizeMisconfiguredIssue<!--/$LogSizeMisconfiguredIssue-->

  Long running transactions: <!--$LongRunningTransactionsIssue-->LongRunningTransactionsIssue<!--/$LongRunningTransactionsIssue-->

  Change data capture job not being run: <!--$CDCReportingIssue-->CDCReportingIssue<!--/$CDCReportingIssue-->

  Change data capture job empty scans: <!--$CDCEmptyScanIssue-->CDCEmptyScanIssue<!--/$CDCEmptyScanIssue-->

  Fast growing log file: <!--$FastGrowingLogIssue-->FastGrowingLogIssue<!--/$FastGrowingLogIssue-->

  

- __Auto-growth turned off__ : Auto-growth is a process during which SQL Server expands the size of a database file once when it runs out of space. The amount of space by which file size will be increased is specified by the __file growth__ option on a database level. If this value is set to zero, this means that file should not be grown once it reaches its limits. To mitigate this issue, use the __MODIFY FILE__ clause of the __ALTER DATABASE__ statement, specifying the __FILEGROWTH__ syntax, as described in the following example:

  ```sql
  alter database database_name
         modify file (name='file_name', filegrowth = 10GB)
  ```

- __Instance storage limit hit__ : This means that managed instance was reaching the preconfigured maximum storage limit. Once when instance storage limit is hit, all insert, update, delete, and index maintenance queries or any other requests that require system or user database space expansion will fail immediately due to the insufficient space. To enable normal operation of your instance, please increase the instance storage size. 

- __Log file size misconfigured__ : This issue means that log file was not configured properly, leaving very small amount of space for the log file itself. To resolve the issue, if you have free, unneeded space on your instance, you can [enlarge your log files](https://docs.microsoft.com/sql/relational-databases/logs/manage-the-size-of-the-transaction-log-file?view=sql-server-ver15#AddOrEnlarge). To enlarge the log file, use the __MODIFY FILE__ clause of the __ALTER DATABASE__ statement, specifying the __SIZE__ syntax, as described in the following example:

  ```sql
  alter database database_name
         modify file (name='file_name', size = 300GB)
  ```

- __Long running transactions__ : Since log truncation includes truncating only __the inactive portion of the transactional log__, having long running transaction causes holding up log truncation and leads to log growing since part of the log file related to this transaction will not be marked as inactive until the transaction completes. Resolving the problem of long active transactions is not straight-forward, and even though killing transaction will resolve your problem, please be very careful with this operation and always consider if letting the transaction to complete normally is an option.

- __Change data capture job not being run__ : Change data capture job, also known as CDC, tracks the INSERT, UPDATE and DELETE operations on the database table, and records detailed information about these changes in a mirrored table, with the same columns structure of the source tables, and additional columns to record the description of these changes. Since CDC job reads from log files, it has to be run frequently in order not to hold up log truncation. On Managed Instance, CDC job is running by default, but customer may pause or stop the job itself. If job is paused by customer, re-enabling the job would mitigate the issue. For more information, please see documentation on [enabling and disabling change data capture job](https://docs.microsoft.com/sql/relational-databases/track-changes/enable-and-disable-change-data-capture-sql-server). 

- __Change data capture job empty scans__ : This error means that CDC job was run successfully but it could not scan the table changes. In most of the cases, this error means that there were underlying DML changes on the table which resulted in the empty scan. For mitigating the issue, please re-enable the CDC job. For more information, please see documentation on [enabling and disabling change data capture job](https://docs.microsoft.com/sql/relational-databases/track-changes/enable-and-disable-change-data-capture-sql-server). 

- __Fast growing log file__ : This means that heavy workload was noticed on the database during reported period, such that with this log growth rate, log file will be full in less than an hour. To enable normal operation of your instance, please revisit the size of your log file and increase the file size if necessary.

## **Recommended Documents**

- [ALTER DATABASE (Transact-SQL) File and Filegroup options](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql-file-and-filegroup-options?view=sql-server-2017)
- [Managing the size of the transactional log file](https://docs.microsoft.com/sql/relational-databases/logs/manage-the-size-of-the-transaction-log-file?view=sql-server-2017#AddOrEnlarge)

