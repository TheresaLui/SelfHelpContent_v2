<properties
	pageTitle="Database connectivity - Failover downtime"
	description="failoverdowntimeshort"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy, VMMicrosoft"
	ms.author="subbuk, vimahadi"
	displayOrder=""
	articleId="FailoverDowntimePlanned_DDE3C31F-19D2-473F-9DDF-5AB905E1F0B0"
	diagnosticScenario="crc_sqldb_connectivity"
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

Building resiliency into your application to account for these situations can help create transparency to the end user when these transient scenarios occur. For information about connectivity in Azure SQL DB, how to implement retry logic, and to understand common errors in Azure SQL DB, please refer to the [database connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors) documentation. Meanwhile, our product team is continually working to minimize these situations and their impact to your database availability.

## **Recommended Documents**

* [Troubleshoot, diagnose, and prevent SQL connection errors and transient errors for SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues)
* [Database connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors)
