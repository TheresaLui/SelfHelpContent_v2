<properties
	pageTitle="Availability and Connectivity/My database was reported as unavailable (Resource Health)"
	description="Availability and Connectivity/My database was reported as unavailable (Resource Health)"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32628802"
	productPesIds="13491"
	cloudEnvironments="public"
/>

# Availability and Connectivity/My database was reported as unavailable (Resource Health)

Resource Health determines the health of your SQL resource by examining the success and failure of logins to the resource every 1-2 minutes. A status of **Unavailable** means that Resource Health has detected consistent login failures due to system error on your SQL Database. A status of **Degraded** means that Resource Health has detected a majority of successful logins, but some failures as well. These login failures may be caused by transient errors.

## **Recommended steps**

* Implementing [retry logic](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues#retry-logic-for-transient-errors) in your client application helps mitigate these situations and should generally make the errors transparent to the end user.<br>
* Check Resource Health blade in the Azure Portal for status updates. When available, downtime reasons for health events are reported in the Health History section of Resource Health. Downtime reasons are typically published 30 minutes after an event.<br>
* If you continue to experience login failures on your SQL Database, please contact support.

## **Recommended documents**

* [Use Resource Health to troubleshoot connectivity for Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-resource-health)<br>
* [Troubleshoot, diagnose, and prevent SQL connection errors](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues)<br>