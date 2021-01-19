<properties
	pageTitle="Failed logins due to compute or storage scaling"
	description="Failed logins due to compute or storage scaling"
	infoBubbleText="Failed logins due to compute or storage scaling"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sqlmi-availability-rca-updateslo"
	diagnosticScenario="SqlMIAvailability"
	selfHelpType="diagnostics"
	supportTopicIds="32746119,32746120,32746121,32746125,32746127,32746128"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI_Availability"
/>
# Failed logins due to compute or storage scaling

## **Failed logins due to compute or storage scaling**
<!--issueDescription-->
We ran diagnostics for managed instance **<!--$ServerName-->ServerName<!--/$ServerName-->** and time period between **<!--$StartTime-->StartTime<!--/$StartTime-->** UTC and **<!--$EndTime-->EndTime<!--/$EndTime-->** UTC and we found failed login(s) caused by instance reconfiguration(s) due to user-initiated **compute or storage scaling**.  
<br>
More details about the failure(s):  
<!--$SQLMIFailedLoginsDueToUpdateSloRcaDetails-->SQLMIFailedLoginsDueToUpdateSloRcaDetails<!--/$SQLMIFailedLoginsDueToUpdateSloRcaDetails-->
<!--/issueDescription-->

SQL Managed Instance is available during update operations, except for a short period of time during the failover that happens at the end of update. This period typically lasts only for a few seconds, even in case of interrupted long-running transactions, due to [accelerated database recovery](https://docs.microsoft.com/azure/azure-sql/accelerated-database-recovery).

## **Recommended Steps**

We don't recommend scale compute or storage of Azure SQL Managed Instance or to change the service tier at the same time with the long-running transactions (data import, data processing jobs, index rebuild, and so on). Database failover that is performed at the end of the operation cancels all ongoing transactions.

Building resiliency into your application to account for these situations can help provide seamless experience for the end user when these transient scenarios occur. For information about connectivity in Azure SQL DB, how to implement retry logic, and to understand common errors in Azure SQL DB, see [database connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors).

## **Recommended Documents**

* [Instance availability during management operations](https://docs.microsoft.com/azure/azure-sql/managed-instance/management-operations-overview?tabs=azure-portal#instance-availability-during-management-operations)

* [Retry logic for transient errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues#retry-logic-for-transient-errors)
