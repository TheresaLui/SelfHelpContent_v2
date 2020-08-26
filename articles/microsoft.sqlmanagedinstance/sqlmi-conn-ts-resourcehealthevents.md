<properties
	pageTitle="Resource Health events"
	description="Resource Health events"
	service="microsoft.sql"
    resource="managedinstances"
    authors="vitomaz-msft"
    ms.author="vitomaz"
	displayOrder=""
	selfHelpType="generic"
    supportTopicIds="32746128"
    productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
	articleId="sqlmi-conn-ts-resourcehealthevents"
	ownershipId="AzureData_AzureSQLMI"
/>

# SQL Managed Instance Resource Health Issues: Unavailability

Resource Health determines the health of your SQL resource by examining the success and failure of logins to the resource every 1-2 minutes. A status of **Unavailable** means that Resource Health has detected consistent login failures due to system error on your SQL Managed Instance. A status of **Degraded** means that Resource Health has detected a majority of successful logins, but some failures as well. These login failures may be caused by transient errors.

## **Recommended Steps**

* Implementing [retry logic](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues#retry-logic-for-transient-errors) in your client application helps mitigate these situations and should generally make the errors transparent to the end user
* Check Resource Health blade in the Azure Portal for status updates. When available, downtime reasons for health events are reported in the Health History section of Resource Health. Downtime reasons are typically published 30 minutes after an event.<br>
* If you continue to experience login failures on your managed instance, please contact support

## **Recommended Documents**

* [Use Resource Health to troubleshoot connectivity](https://docs.microsoft.com/azure/sql-database/sql-database-resource-health)<br>
* [Troubleshoot, diagnose, and prevent SQL connection errors](https://docs.microsoft.com/azure/sql-database/troubleshoot-connectivity-issues-microsoft-azure-sql-database)<br>
