<properties
	pageTitle="Failed logins due to planned updates"
	description="Failed logins due to planned updates"
	infoBubbleText="Failed logins due to planned updates"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sqlmi-availability-rca-plannedupgrades"
	diagnosticScenario="SqlMIAvailability"
	selfHelpType="diagnostics"
	supportTopicIds="32746119,32746120,32746121,32746125,32746127,32746128"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI_Availability"
/>
# Failed logins due to planned updates

## **Failed logins due to planned maintenance**
<!--issueDescription-->
We ran diagnostics for managed instance **<!--$ServerName-->ServerName<!--/$ServerName-->** and time period between **<!--$StartTime-->StartTime<!--/$StartTime-->** UTC and **<!--$EndTime-->EndTime<!--/$EndTime-->** UTC. We found failed logins caused by instance reconfigurations due to **planned maintenance**.  
<br>
**More details about the failures:**  
<!--$SQLMIFailedLoginsDueToUpgradeRCADetails-->SQLMIFailedLoginsDueToUpgradeRCADetails<!--/$SQLMIFailedLoginsDueToUpgradeRCADetails-->
<!--/issueDescription-->
<br>
The Azure infrastructure can dynamically reconfigure servers for planned operations such as load balancing and updates, or unplanned events such as recoveries from software or hardware issues. In this case, the reconfiguration happened due to **planned maintenance**. Most reconfiguration events take less than 60 seconds to complete. We are working continually on minimizing the incidence of updates and their impact on instance availability.

The maintenance window feature provides you with the ability to onboard Azure SQL resource to prescheduled time blocks outside of business hours. See [maintenance window](https://docs.microsoft.com/azure/azure-sql/database/maintenance-window) for more information.

## **Recommended Steps** 

Building resiliency into your application to account for these situations can help provide seamless experience for end users. For more information about Azure SQL, including connectivity, how to implement retry logic, and common errors, see [database connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors).

## **Recommended Documents**

* [Troubleshoot, diagnose, and prevent SQL connection errors and transient errors for SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues)

* [Retry logic for transient errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues#retry-logic-for-transient-errors)

* [Maintenance window](https://docs.microsoft.com/azure/azure-sql/database/maintenance-window)
