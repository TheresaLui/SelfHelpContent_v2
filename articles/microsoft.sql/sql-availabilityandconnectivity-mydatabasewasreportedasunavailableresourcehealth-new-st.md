<properties
	pageTitle="SQL Database Resource Health Issues: Unavailability"
	description="SQL Database Resource Health Issues: Unavailability"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
  	ms.author="emlisa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32745438"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
	articleId="ec03f2ee-fbd5-4879-9f4f-73b76f7f22d4-new-st"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# SQL Database Resource Health Issues: Unavailability

Resource Health determines the health of your SQL resource by examining the success and failure of logins to the resource every 1-2 minutes. A status of **Unavailable** means that Resource Health has detected consistent login failures due to system error on your SQL Database. A status of **Degraded** means that Resource Health has detected a majority of successful logins, but some failures as well. These login failures may be caused by transient errors.

## **Recommended Steps**

* Implementing [retry logic](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues?WT.mc_id=pid:13491:sid:32745438/#retry-logic-for-transient-errors) in your client application helps mitigate these situations and should generally make the errors transparent to the end user
* Check Resource Health blade in the Azure Portal for status updates. When available, downtime reasons for health events are reported in the Health History section of Resource Health. Downtime reasons are typically published two and a half hours after an event.<br>
* If you continue to experience login failures on your SQL Database, please contact support

## **Recommended Documents**

* [Use Resource Health to troubleshoot connectivity for Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-resource-health?WT.mc_id=pid:13491:sid:32745438/)<br>
* [Troubleshoot, diagnose, and prevent SQL connection errors](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database?WT.mc_id=pid:13491:sid:32745438/)<br>
