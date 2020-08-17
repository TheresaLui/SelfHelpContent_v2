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
	diagnosticScenario="sqlmi-availability-rca-updateslo"
	selfHelpType="diagnostics"
	supportTopicIds="32739488,32637246,32637259,32637254"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI"
/>
# Failed logins due to compute or storage scaling

## ** Failed logins due to compute or storage scaling **
<!--issueDescription-->
We ran diagnostics on instance **<!--$ServerName-->ServerName<!--/$ServerName-->** between **<!--$StartTime-->StartTime<!--/$StartTime-->** UTC and **<!--$EndTime-->EndTime<!--/$EndTime-->** UTC and we found failed login(s) caused by reconfiguration(s) due to **compute or storage scaling**.  
<br>
More details about the failure(s):  
<!--$SQLMIFailedLoginsDueToUpdateSloRcaDetails-->SQLMIFailedLoginsDueToUpdateSloRcaDetails<!--/$SQLMIFailedLoginsDueToUpdateSloRcaDetails-->
<!--/issueDescription-->

## **Recommended Steps**

SQL Managed Instance is available during update operations, except a short downtime caused by the failover that happens at the end of update. It typically lasts up to 10 seconds even in case of interrupted long-running transactions, thanks to the [accelerated database recovery](https://docs.microsoft.com/azure/azure-sql/accelerated-database-recovery).

It's not recommended to scale compute or storage of Azure SQL Managed Instance or to change the service tier at the same time with the long-running transactions (data import, data processing jobs, index rebuild, etc.). Database failover that will be performed at the end of the operation will cancel all ongoing transactions.

Building resiliency into your application to account for these situations can help create transparency to the end user when these transient scenarios occur. For information about connectivity in Azure SQL DB, how to implement retry logic, and to understand common errors in Azure SQL DB please refer to this article on [database connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors).

## **Recommended Documents**

* [Instance availability during management operations](https://docs.microsoft.com/azure/azure-sql/managed-instance/management-operations-overview?tabs=azure-portal#instance-availability-during-management-operations)

* [Retry logic for transient errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues#retry-logic-for-transient-errors)