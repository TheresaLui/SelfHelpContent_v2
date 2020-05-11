<properties
	pageTitle="SQL Database Resource Health Issues: Unavailability"
	description="SQL Database Resource Health Issues: Unavailability"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
  ms.author="emlisa"
	displayOrder="2"
	selfHelpType="generic"
	supportTopicIds="32630438"
	productPesIds="13491"
	cloudEnvironments="MoonCake"
    resourceTags="servers, databases"
	articleId="sql-availabilityandconnectivity-mydatabasewasreportedasunavailableresourcehealth-mooncake"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# SQL Database Resource Health Issues: Unavailability

Resource Health determines the health of your SQL resource by examining the success and failure of logins to the resource every 1-2 minutes. A status of **Unavailable** means that Resource Health has detected consistent login failures due to system error on your SQL Database. A status of **Degraded** means that Resource Health has detected a majority of successful logins, but some failures as well. These login failures may be caused by transient errors.

## **Recommended Steps**

* Implementing [retry logic](https://docs.azure.cn/sql-database/sql-database-connectivity-issues#retry-logic-for-transient-errors?WT.mc_id=pid:13491:sid:32630438/) in your client application helps mitigate these situations and should generally make the errors transparent to the end user
* Check Resource Health blade in the Azure Portal for status updates. When available, downtime reasons for health events are reported in the Health History section of Resource Health. Downtime reasons are typically published 30 minutes after an event.
* If you continue to experience login failures on your SQL Database, please contact support

## **Recommended Documents**

* [Use Resource Health to troubleshoot connectivity for Azure SQL Database](https://docs.azure.cn/sql-database/sql-database-resource-health?WT.mc_id=pid:13491:sid:32630438/)
* [Troubleshoot, diagnose, and prevent SQL connection errors](https://docs.azure.cn/sql-database/sql-database-connectivity-issues?WT.mc_id=pid:13491:sid:32630438/)
