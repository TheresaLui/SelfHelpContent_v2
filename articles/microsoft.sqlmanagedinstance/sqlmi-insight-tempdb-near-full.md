<properties
	pageTitle="Managed Instance - Tempdb nearly full"
	description="Managed Instance - Tempdb nearly full"
	infoBubbleText="Tempdb allocated space is nearing the max space. See details on the right."
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="miobrado"
	authors="miobrado"
	displayOrder=""
	diagnosticScenario="SqlMIPerf_TempdbNearFull"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmanagedinstance-perf-tempdb-near-full"
	ownershipId="AzureData_AzureSQLMI"
/>

# Managed Instance - Tempdb nearly full

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Managed Instance named <!--$ServerName-->ServerName<!--/$ServerName--> on the subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> and the resource group <!--$ResourceGroup-->ResourceGroup<!--/$ResourceGroup--> was facing a potential problem between <!--$startTime-->startTime<!--/$startTime--> and <!--$endTime-->endTime<!--/$endTime--> where tempdb was getting full. We have detected that <!--$totalSpaceAllocatedPct-->totalSpaceAllocatedPct<!--/$totalSpaceAllocatedPct-->% of max tempdb size was allocated and <!--$totalSpaceUsedPct-->totalSpaceUsedPct<!--/$totalSpaceUsedPct-->% of the allocated space used.
<!--/issueDescription-->

The tempdb is a global resource that is shared by all users connected to the instance. When SQL Server Database Engine runs out of tempdb space, query execution may start failing and transactions may be rolled back with a corresponding error. For example:

  - **1104** No disk space available in tempdb. Create space by dropping objects and/or rewrite the query to consume fewer rows. If the issue still persists, consider upgrading to a higher service level objective.
  - **3958** Transaction aborted when accessing versioned row. Requested versioned row was not found. Your tempdb is probably out of space. Please refer to BOL on how to configure tempdb for versioning.
  - **3959** Version store is full. New versions could not be added. A transaction that needs to access the version store may be rolled back. Please refer to BOL on how to configure tempdb for versioning.
  - **3966** Transaction is rolled back when accessing version store. It was marked as a victim because it may need the row versions that have already been removed to make space in tempdb. Not enough disk space allocated for tempdb, or transaction running for too long and may potentially need the version that has been removed to make space in the version store. Allocate more space for tempdb, or make transactions shorter.

## **Recommended Steps**

* If the allocated space is not used, run `DBCC SHRINKFILE` to shrink the tempdb file size.
* If the allocated space is used, failover the instance to clean tempdb completely and restore its default configuration. You can failover the instance using REST API, PowerShell or Azure CLI.

## **Recommended Documents**

* [tempdb](https://docs.microsoft.com/sql/relational-databases/databases/tempdb-database)
* [DBCC SHRINKFILE](https://docs.microsoft.com/sql/t-sql/database-console-commands/dbcc-shrinkfile-transact-sql)
* [REST API - Managed Instance failover](https://docs.microsoft.com/rest/api/sql/managed%20instances%20-%20failover/failover)
* [Az PowerShell - Managed Instance failover](https://docs.microsoft.com/powershell/module/az.sql/Invoke-AzSqlInstanceFailover?view=azps-4.4.0)
* [Azure CLI - Managed Instance failover](https://docs.microsoft.com/cli/azure/sql/mi?view=azure-cli-latest#az-sql-mi-failover)
