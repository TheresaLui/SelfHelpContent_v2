<properties
	pageTitle="Failover due to planned updates"
	description="Failover due to planned updates"
	infoBubbleText="Failover due to planned updates"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sqlmi-availability-rca-failover-plannedupgrades"
	diagnosticScenario="SqlMIAvailability"
	selfHelpType="diagnostics"
	supportTopicIds="32746119,32746120,32746121,32746125,32746127,32746128"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI"
/>
# Failover due to planned updates

## **Failover due to planned updates**
<!--issueDescription-->
We ran diagnostics for managed instance **<!--$ServerName-->ServerName<!--/$ServerName-->** and time period between **<!--$StartTime-->StartTime<!--/$StartTime-->** UTC and **<!--$EndTime-->EndTime<!--/$EndTime-->** UTC and we found instance reconfiguration(s) due to **planned updates**.  
<br>
More details:  
<!--$SQLMIFailoverDueToUpgradeRCADetails-->SQLMIFailoverDueToUpgradeRCADetails<!--/$SQLMIFailoverDueToUpgradeRCADetails-->
<!--/issueDescription-->

The Azure infrastructure can dynamically reconfigure servers for planned operations such as load balancing and updates, or unplanned events such as recoveries from software or hardware issues. In this case, the reconfiguration happened due to **planned updates**. Most reconfiguration events take less than 60 seconds to complete. We are working continually on minimizing incidence of updates and their impact to instance availability.

## **Recommended Steps** 

Building resiliency into your application to account for these situations can help provide seamless experience for the end users. For information about connectivity in Azure SQL, how to implement retry logic, and to understand common errors in Azure SQL please refer to the [database connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors) article.

## **Recommended Documents**

* [Troubleshoot, diagnose, and prevent SQL connection errors and transient errors for SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues)

* [Retry logic for transient errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues#retry-logic-for-transient-errors)