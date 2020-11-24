<properties
	pageTitle="Failover due to compute or storage scaling"
	description="Failover due to compute or storage scaling"
	infoBubbleText="Failover due to compute or storage scaling"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sqlmi-availability-rca-failover-updateslo"
	diagnosticScenario="SqlMIAvailability"
	selfHelpType="diagnostics"
	supportTopicIds="32746119,32746120,32746121,32746125,32746127,32746128"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI"
/>
# Failover due to compute or storage scaling

## **Failover due to compute or storage scaling**
<!--issueDescription-->
We ran diagnostics for managed instance **<!--$ServerName-->ServerName<!--/$ServerName-->** and time period between **<!--$StartTime-->StartTime<!--/$StartTime-->** UTC and **<!--$EndTime-->EndTime<!--/$EndTime-->** UTC and we found instance reconfiguration(s) due to user-initiated **compute or storage scaling**.  
<br>
More details:  
<!--$SQLMIFailoverDueToUpdateSloRcaDetails-->SQLMIFailoverDueToUpdateSloRcaDetails<!--/$SQLMIFailoverDueToUpdateSloRcaDetails-->
<!--/issueDescription-->

SQL Managed Instance is available during update operations, except a short period of time during the failover that happens at the end of update. It typically lasts seconds even in case of interrupted long-running transactions, thanks to the [accelerated database recovery](https://docs.microsoft.com/azure/azure-sql/accelerated-database-recovery).

## **Recommended Steps**
It's not recommended to scale compute or storage of Azure SQL Managed Instance or to change the service tier at the same time with the long-running transactions (data import, data processing jobs, index rebuild, etc.). Database failover that will be performed at the end of the operation will cancel all ongoing transactions.

Building resiliency into your application to account for these situations can help provide seamless experience for the end user when these transient scenarios occur. For information about connectivity in Azure SQL DB, how to implement retry logic, and to understand common errors in Azure SQL DB please refer to the [database connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors) article.

## **Recommended Documents**

* [Instance availability during management operations](https://docs.microsoft.com/azure/azure-sql/managed-instance/management-operations-overview?tabs=azure-portal#instance-availability-during-management-operations)

* [Retry logic for transient errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues#retry-logic-for-transient-errors)