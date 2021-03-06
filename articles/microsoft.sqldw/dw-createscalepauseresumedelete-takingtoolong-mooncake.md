<properties
	pageTitle="Create/Scale/Pause/Resume/Delete operation taking too long"
	description="Create/Scale/Pause/Resume/Delete operation taking too long"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	supportTopicIds=""
	productPesIds=""
	displayOrder="4"
	selfHelpType="resource"
	resourceTags="datawarehouse"
	articleId="dw-createscalepauseresumedelete-takingtoolong-mooncake"
	cloudEnvironments="MoonCake"
	ownershipId="AzureData_AzureSQLDB"
/>
# Create/Scale/Pause/Resume/Delete database taking too long

## **Recommended Steps**

Issues connecting to SQL Data Warehouse can occur for a number of reasons, including incorrect firewall configuration, connection strings, or maintenance periods. If you are having issues with a client tool, please ensure you have the latest version of the tool and [visit the following documentation](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-troubleshoot#tools).

Persistent connection issues to Azure SQL Database can occur due to incorrect firewall configuration, incorrect connection string, and other causes.

Resource Health determines the health of your SQL resource by examining the success and failure of logins to the resource every 1-2 minutes. A status of Unavailable means that Resource Health has detected consistent login failures due to system error on your SQL Database. A status of Degraded means that Resource Health has detected a majority of successful logins, but some failures as well. These login failures may be caused by transient errors.

* Check [Microsoft Azure Service Dashboard](https://www.azure.cn/support/service-dashboard/) for any known issues
* Check [Resource Health](https://docs.azure.cn/service-health/resource-health-overview) blade in the Azure Portal for status updates. When available, downtime reasons for health events are reported in the Health History section of Resource Health. Downtime reasons are typically published 30 minutes after an event.
* [Configure firewall rules](https://docs.azure.cn/sql-data-warehouse/create-data-warehouse-portal#create-a-server-level-firewall-rule)
* [Configure Azure AD authentication](https://docs.azure.cn/sql-database/sql-database-aad-authentication-configure?WT.mc_id=pid:13491:sid:32630414/)
* [Configure multi-factor authentication for Azure AD](https://docs.azure.cn/sql-database/sql-database-ssms-mfa-authentication-configure?WT.mc_id=pid:13491:sid:32630414/)
* [Verify the connection string](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-connect-overview#find-your-server-name) from the portal
* Use the [available PowerShell commands](https://docs.microsoft.com/powershell/module/azurerm.sql/?view=azurermps-6.3.0#sql)
* Implementing [retry logic](https://docs.azure.cn/sql-database/sql-database-connectivity-issues#retry-logic-for-transient-errors) in your client application helps mitigate these situations and should generally make the errors transparent to the end user

## **Recommended Documents**

* [Additional Troubleshooting](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-troubleshoot)
* [Create a server-level firewall rule](https://docs.azure.cn/sql-data-warehouse/create-data-warehouse-portal#create-a-server-level-firewall-rule)
* [Use virtual network service endpoints](https://docs.azure.cn/sql-database/sql-database-vnet-service-endpoint-rule-overview?toc=/azure/sql-data-warehouse/toc.json)
* [View maintenance schedule](https://docs.azure.cn/sql-data-warehouse/viewing-maintenance-schedule)
* [Change maintenance schedule](https://docs.azure.cn/sql-data-warehouse/changing-maintenance-schedule)
* [Connect and manage your Data Warehouse using the Azure portal](https://docs.azure.cn/sql-data-warehouse/create-data-warehouse-portal)
* [Connect and manage your Data Warehouse using PowerShell](https://docs.azure.cn/sql-data-warehouse/create-data-warehouse-powershell)
* [Pause and resume from Azure portal](https://docs.azure.cn/sql-data-warehouse/pause-and-resume-compute-portal)
* [Pause and resume from PowerShell](https://docs.azure.cn/sql-data-warehouse/pause-and-resume-compute-powershell)
* [Manage compute](https://docs.azure.cn/sql-data-warehouse/sql-data-warehouse-manage-compute-overview)
* [Scale from Azure portal](https://docs.azure.cn/sql-data-warehouse/quickstart-scale-compute-portal)
* [Scale from PowerShell](https://docs.azure.cn/sql-data-warehouse/quickstart-scale-compute-powershell)
* [Scale from T-SQL](https://docs.azure.cn/sql-data-warehouse/quickstart-scale-compute-tsql)
* [Clean up resources](https://docs.azure.cn/sql-data-warehouse/pause-and-resume-compute-powershell#clean-up-resources)
* [Debugging ARM template deployments](https://azure.microsoft.com/blog/debugging-arm-template-deployments?WT.mc_id=pid:13491:sid:32630406/)
