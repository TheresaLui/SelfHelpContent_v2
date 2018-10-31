<properties
	pageTitle="Database connectivity - Failover downtime"
	description="failoverdowntimeshort"
	infoBubbleText="Found recent connectivity issue. See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="subbu-kandhaswamy"
	displayOrder=""
	articleId="FailoverDowntimeUnplanned_518F0886-57CD-42A7-B526-77900A8C0D9D"
	diagnosticScenario="crc_sqldb_connectivity"
	selfHelpType="rca"
	supportTopicIds="31980414"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$startTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> the database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName--> experienced <!--$FailoverCount-->FailoverCount<!--/$FailoverCount--> reconfiguration(s). The total time of unavailability caused by these reconfiguration(s) was <!--$FailoverTotalSeconds-->FailoverTotalSeconds<!--/$FailoverTotalSeconds--> seconds.

The Azure infrastructure has the ability to dynamically reconfigure servers for planned operations such as load balancing and updates or unplanned occurrences such as health recoveries from software or hardware issues. In this scenario this was due to unplanned operation(s) specifically related to <!--$FailoverUnplannedReason-->FailoverUnplannedReason<!--/$FailoverUnplannedReason-->.  In general, reconfigurations are short in duration and below 60 seconds.
<!--/issueDescription-->

Building in resiliency to your application to account for these situations can help create transparency to the end user when these transient scenarios occur. For  information about connectivity in Azure SQL DB, how to implement Retry Logic, and to understand common errors in Azure SQL DB refer - https://docs.microsoft.com/en-us/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors. Meanwhile our product team is constantly working to minimize these situations and their impact to your database availability.

## **Recommended Documents**

* [Troubleshoot, diagnose, and prevent SQL connection errors and transient errors for SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues)

* [Database-connection-errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors)
