<properties
	pageTitle="Managed Instance - Large Tempdb Usage due to Query"
	description="Managed Instance - Large Tempdb Usage due to Query"
	infoBubbleText="Some queries are using a lot of tempdb space. See details on the right."
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="miobrado"
	authors="miobrado"
	displayOrder=""
	diagnosticScenario="SqlMIPerf_LargeTempdbUsageDueToQuery"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmanagedinstance-perf-tempdb-large-usage-due-to-query"
	ownershipId="AzureData_AzureSQLMI"
/>

# Managed Instance - Large Tempdb Usage due to Query

## We ran diagnostics on your resource and found a potential issue

<!--issueDescription-->
Managed Instance named <!--$ServerName-->ServerName<!--/$ServerName--> on the subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and the resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> was facing a potential problem between <!--$startTime-->startTime<!--/$startTime--> and <!--$endTime-->endTime<!--/$endTime--> where some queries were using a lot of tempdb space. Detected query hash codes: <!--$listQueryHash-->listQueryHash<!--/$listQueryHash-->. Detected tempdb usage (GB): <!--$listTempdbUsedByQueryGB-->listTempdbUsedByQueryGB<!--/$listTempdbUsedByQueryGB-->. Detected tempdb usage (%): <!--$listTempdbUsedByQueryPct-->listTempdbUsedByQueryPct<!--/$listTempdbUsedByQueryPct-->.
<!--/issueDescription-->

The tempdb is a global resource that is shared by all users connected to the instance. When SQL Server Database Engine runs out of tempdb space, query execution may start failing and transactions may be rolled back with a corresponding error. For example:

  - **1104** No disk space available in tempdb. Create space by dropping objects and/or rewrite the query to consume fewer rows. If the issue still persists, consider upgrading to a higher service level objective.
  - **3958** Transaction aborted when accessing versioned row. Requested versioned row was not found. Your tempdb is probably out of space. Please refer to BOL on how to configure tempdb for versioning.
  - **3959** Version store is full. New versions could not be added. A transaction that needs to access the version store may be rolled back. Please refer to BOL on how to configure tempdb for versioning.
  - **3966** Transaction is rolled back when accessing version store. It was marked as a victim because it may need the row versions that have already been removed to make space in tempdb. Not enough disk space allocated for tempdb, or transaction running for too long and may potentially need the version that has been removed to make space in the version store. Allocate more space for tempdb, or make transactions shorter.

## **Recommended Steps**

* Consider rewriting the queries identified by the query hash codes listed above to consume fewer rows
* Consider running `DBCC SHRINKFILE` to shrink the tempdb file size

## **Recommended Documents**

* [tempdb](https://docs.microsoft.com/sql/relational-databases/databases/tempdb-database)
* [How to shrink the tempdb database in SQL Server](https://support.microsoft.com/help/307487/how-to-shrink-the-tempdb-database-in-sql-server)
* [DBCC SHRINKFILE](https://docs.microsoft.com/sql/t-sql/database-console-commands/dbcc-shrinkfile-transact-sql)
