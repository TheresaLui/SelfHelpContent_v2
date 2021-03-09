<properties
	pageTitle="Database connectivity - Failover downtime LongRecovery"
	description="failoverlongrecovery"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy, VMMicrosoft"
	ms.author="subbuk, vimahadi"
	displayOrder=""
	articleId="PlanedFailoverLR_1FBC4A97-DC3A-4DF9-86C0-46B00AF0F733"
	diagnosticScenario="SqlConnectivity"
	selfHelpType="rca"
	supportTopicIds="31980414"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime-->, the database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName--> experienced <!--$FailoverCount-->FailoverCount<!--/$FailoverCount--> reconfiguration(s). The total time of unavailability caused by these reconfiguration(s) was <!--$FailoverTotalSeconds-->FailoverTotalSeconds<!--/$FailoverTotalSeconds--> seconds.

The Azure infrastructure has the ability to dynamically reconfigure servers for planned operations such as load balancing and updates, or unplanned occurrences such as recoveries from software or hardware issues. In this instance, the reconfiguration was due to planned operation(s) specifically related to <!--$FailoverPlannedReason-->FailoverPlannedReason<!--/$FailoverPlannedReason-->. Most reconfiguration events take less than 60 seconds to complete.
<!--/issueDescription-->

In this instance, the longest part of the reconfiguration duration totaled <!--$RecoveryDuration-->RecoveryDuration<!--/$RecoveryDuration--> seconds. This was due to a long recovery of transactions that were running on the database at the time of the reconfiguration. As Azure SQL Databases need to maintain transactional consistency, transactions that are in flight during this operation will need to roll back and, if large in size, can take a longer time to complete. While this is expected behavior, implementing best practices such as batching transactions to smaller sizes will result in less recovery time when these reconfiguration operations occur.

In addition, building resiliency into your application to account for these situations can help create transparency to the end user when these transient scenarios occur. For information about connectivity in Azure SQL DB, how to implement retry logic, and to understand common errors in Azure SQL DB, please refer to this article on [database connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors). Our product team is continually working to minimize these situations and their impact to your database availability.

## **Recommended Documents**

* [Database connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors)
* [How to use batching to improve SQL Database application performance](https://docs.microsoft.com/azure/sql-database/sql-database-use-batching-to-improve-performance)
* [Troubleshoot, diagnose, and prevent SQL connection errors and transient errors for SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues)
