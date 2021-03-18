<properties
	pageTitle="Failed logins due to unplanned operation(s)"
	description="Failed logins due to unplanned operation(s)"
	infoBubbleText="Failed logins due to unplanned operation(s)"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sqlmi-availability-rca-unplanned"
	diagnosticScenario="SqlMIAvailability"
	selfHelpType="diagnostics"
	supportTopicIds="32746119,32746120,32746121,32746125,32746127,32746128"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI_Availability"
/>
# Failed logins due to unplanned operation(s)

## **Failed logins due to unplanned operation(s)**
<!--issueDescription-->
We ran diagnostics on instance **<!--$ServerName-->ServerName<!--/$ServerName-->** between **<!--$StartTime-->StartTime<!--/$StartTime-->** UTC and **<!--$EndTime-->EndTime<!--/$EndTime-->** UTC and we found failed login(s) caused by reconfiguration(s) due to **unplanned operation(s)**.  
<br>
More details about the failure(s):  
<!--$SQLMIFailedLoginsDueToUnplannedEventRcaDetails-->SQLMIFailedLoginsDueToUnplannedEventRcaDetails<!--/$SQLMIFailedLoginsDueToUnplannedEventRcaDetails-->
<!--/issueDescription-->

## **Recommended Steps**

The Azure infrastructure has the ability to dynamically reconfigure servers for planned operations such as load balancing and updates, or unplanned occurrences such as recoveries from software or hardware issues. In this instance, the reconfiguration was due to **unplanned operation(s)**. Most reconfiguration events take less than 60 seconds to complete.   

Building resiliency into your application to account for these situations can help create transparency to the end user when these transient scenarios occur. For information about connectivity in Azure SQL DB, how to implement retry logic, and to understand common errors in Azure SQL DB, see [database connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors). Meanwhile, our product team is continually working to minimize these situations and their impact on your database availability.   

## **Recommended Documents**

* [Troubleshoot, diagnose, and prevent SQL connection errors and transient errors for SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues)

* [Retry logic for transient errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues#retry-logic-for-transient-errors)
