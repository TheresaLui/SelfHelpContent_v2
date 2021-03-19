<properties
	pageTitle="Managed Instance - Configuration settings disabled"
	description="Managed Instance - Configuration settings disabled"
	infoBubbleText="Managed Instance noticed to have some configuration settings disabled"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="zlradeti"
	authors="zlradeti"
	displayOrder=""
	diagnosticScenario="SqlMIPerf_Configs_Disabled"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="sqlmanagedinstance-perf-disabled-settings"
	ownershipId="AzureData_AzureSQLMI"
/>

# Managed Instance - Configuration settings disabled

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed instance named <!--$ServerName-->ServerName<!--/$ServerName--> on subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> was  noticed to have some configuration settings disabled between <!--$startTime-->startTime<!--/$startTime--> and <!--$endTime-->endTime<!--/$endTime-->, which could result in a heavy performance impact on the customer's workload.

<!--/issueDescription-->

## **Recommended Steps**

- Recommended steps strongly depend on the disabled setting. Because of this, please check the following list of the affected databases and the issues noticed on them, and then continue with recommended steps depending on the setting which was disabled.

  

  Affected databases: <!--$AffectedDatabases-->AffectedDatabases<!--/$AffectedDatabases-->

  Query Data Store Issues: <!--$QdsStats-->QdsStats<!--/$QdsStats-->

  Force Last Good Plan Issues: <!--$AprcStats-->AprcStats<!--/$AprcStats-->

  Auto Stats Issues: <!--$AutoStats-->AutoStats<!--/$AutoStats-->

  MAXDOP Issues: <!--$MaxDopStats-->MaxDopStats<!--/$MaxDopStats-->

  

- __Query Data Store__ : The SQL Server Query Store feature provides you with insight on query plan choice and performance. It simplifies performance troubleshooting by helping you quickly find performance differences caused by query plan changes. Query Store automatically captures a history of queries, plans, and runtime statistics, and retains these for your review. If query store is disabled, please consider enabling it:

  ```sql
  ALTER DATABASE database_name
        SET QUERY_STORE = ON (OPERATION_MODE = READ_WRITE);
  ```

- __Force Last Good Plan Issues__ :  Identifies Azure SQL queries using an execution plan that is slower than the previous good plan, and queries using the last known good plan instead of the regressed plan. If Force Last Good Plan feature is disabled, please consider enabling it: 

  ```sql
  ALTER DATABASE database_name
       SET AUTOMATIC_TUNING ( FORCE_LAST_GOOD_PLAN = ON ); 
  ```

- __Auto Stats__ : When the automatic create and update statistics options are ON, the Query Optimizer creates and updates statistics on individual columns in the query predicate, as necessary, to improve cardinality estimates for the query plan. If auto create and update statistics are disabled, consider enabling them: 

  ```sql
  ALTER DATABASE database_name 
  	SET auto_create_statistics ON 
  
  ```

- __MAXDOP__:  When an instance of SQL Server runs on a computer that has more than one microprocessor or CPU, it detects the degree of parallelism, that is, the number of processors employed to run a single statement, for each parallel plan execution. You can use the **max degree of parallelism** option to limit the number of processors to use in parallel plan execution. Since huge MAXDOP can cause heavy waits between parallel producers and consumers, it is highly recommended that on SQL Managed Instance MAXDOP stays between 1 and 8. Have on mind that value 0 means 'Use all available cores' and is not recommended, especially for high number of cores on which SQL Server instance is running. To manage MAXDOP setting, you can use following T-SQL statement: 

  ```sql
    ALTER DATABASE SCOPED CONFIGURATION SET MAXDOP = 8
  ```

## **Recommended Documents**

* [Automatic Tuning](https://docs.microsoft.com/sql/relational-databases/automatic-tuning/automatic-tuning?view=sql-server-2017)
* [SQL Server Statistics Overview](https://docs.microsoft.com/sql/relational-databases/statistics/statistics?view=sql-server-2017)
* [Turn on Auto Update Statistics](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql-set-options?view=sql-server-2017#auto_update_statistics)
* [Turn on Auto Create Statistics](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql-set-options?view=sql-server-2017#auto_update_statistics)
* [Tune Azure SQL MAXDOP setting with Alter Database](https://docs.microsoft.com/sql/t-sql/statements/alter-database-scoped-configuration-transact-sql?view=sql-server-2017)
* [Monitoring Performance by using the Query Store](https://docs.microsoft.com/sql/relational-databases/performance/monitoring-performance-by-using-the-query-store?view=sql-server-ver15)
