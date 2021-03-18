<properties
	pageTitle="Failover due to user initiated manual failover"
	description="Failover due to user initiated manual failover"
	infoBubbleText="Failover due to user initiated manual failover"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sqlmi-availability-rca-failover-manualfaillover"
	diagnosticScenario="SqlMIAvailability"
	selfHelpType="diagnostics"
	supportTopicIds="32746119,32746120,32746121,32746125,32746127,32746128"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI_Availability"
/>
# Failover due to user initiated manual failover

## **Failover due to user initiated manual failover**
<!--issueDescription-->
We ran diagnostics for the managed instance **<!--$ServerName-->ServerName<!--/$ServerName-->** and for the time period between **<!--$StartTime-->StartTime<!--/$StartTime-->** UTC and **<!--$EndTime-->EndTime<!--/$EndTime-->** UTC and we found instance reconfiguration(s) due to **user initiated manual failover(s)**.  
<br>
For more details, see:  
<!--$SQLMIFailoverDueToManualFailoverRCADetails-->SQLMIFailoverDueToManualFailoverRCADetails<!--/$SQLMIFailoverDueToManualFailoverRCADetails-->
<!--/issueDescription-->   
<br><br>
High availability is a fundamental part of the SQL Database and SQL Managed Instance platform that works transparently for your database application. However, we realize that you may want to test how the automatic failover operations initiated during planned or unplanned events would impact an application before you deploy it to production. You can manually trigger a failover by calling a special API to restart a managed instance. The failovesr listed above are the result of user-initiated manual failover(s). Most reconfiguration events take less than 60 seconds to complete. We are working continually to minimize the incidence of updates and their impacts on instance availability. 

## **Recommended Steps** 

Building resiliency into your application to account for these situations can help provide a seamless experience for the end users. For information about connectivity in Azure SQL, how to implement retry logic, and to understand common errors in Azure SQL, see [database connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages#database-connection-errors-transient-errors-and-other-temporary-errors).

## **Recommended Documents**

* [User-initiated manual failover on SQL Managed Instance](https://techcommunity.microsoft.com/t5/azure-sql-database/user-initiated-manual-failover-on-sql-managed-instance/ba-p/1538803)

* [Retry logic for transient errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues#retry-logic-for-transient-errors)
