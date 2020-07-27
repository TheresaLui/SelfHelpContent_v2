<properties
	pageTitle="Availability and Connectivity/Data Warehouse is stuck during creation, scaling or resuming"
	description="Availability and Connectivity/Data Warehouse is stuck during creation, scaling or resuming"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	supportTopicIds="32635193"
	productPesIds="15818"
	displayOrder="1"
	selfHelpType="generic"
	resourceTags=""
	articleId="dw-availabilityandconnectivity-dwisstuckduringcreationscalingorresuming.md"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# Data Warehouse is stuck during creation, scaling, or resuming

## **Recommended Steps**

Issues connecting to SQL Data Warehouse can occur for a number of reasons, including incorrect firewall configuration, connection strings, or maintenance periods. If you are having issues with a client tool, please ensure you have the latest version of the tool and [visit the following documentation](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot#tools).<br>

Persistent connection issues to Azure SQL Database can occur due to incorrect firewall configuration, incorrect connection string, and other causes.<br>

Resource Health determines the health of your SQL resource by examining the success and failure of logins to the resource every 1-2 minutes. A status of **Unavailable** means that Resource Health has detected consistent login failures due to system error on your SQL Database. A status of **Degraded** means that Resource Health has detected a majority of successful logins, but some failures as well. These login failures may be caused by transient errors.

* Check [Microsoft Azure Service Dashboard](https://azure.microsoft.com/status/) for any known issues<br>
* Check [Resource Health](https://docs.microsoft.com/azure/service-health/resource-health-overview) blade in the Azure Portal for status updates. When available, downtime reasons for health events are reported in the Health History section of Resource Health. Downtime reasons are typically published 30 minutes after an event.<br>
* [Configure firewall rules](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-portal#create-a-server-level-firewall-rule)<br>
* [Configure Azure AD authentication](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?WT.mc_id=pid:13491:sid:32745423/)<br>
* [Configure multi-factor authentication for Azure AD](https://docs.microsoft.com/azure/sql-database/sql-database-ssms-mfa-authentication-configure?WT.mc_id=pid:13491:sid:32745423/)<br>
* [Verify the connection string](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-connect-overview#find-your-server-name) from the portal<br>
* Use the [available PowerShell commands](https://docs.microsoft.com/powershell/module/azurerm.sql/?view=azurermps-6.3.0#sql)<br>
* Implementing [retry logic](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues#retry-logic-for-transient-errors) in your client application helps mitigate these situations and should generally make the errors transparent to the end user.

## **Recommended Documents**

* [Troubleshooting connectivity issues](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity)<br>
* [Additional Troubleshooting](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-troubleshoot/)<br>
* [Create a server-level firewall rule](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-portal#create-a-server-level-firewall-rule)<br>
* [Use virtual network service endpoints](https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview?toc=/azure/sql-data-warehouse/toc.json)<br>
* [View maintenance schedule](https://docs.microsoft.com/azure/sql-data-warehouse/viewing-maintenance-schedule)<br>
* [Change maintenance schedule](https://docs.microsoft.com/azure/sql-data-warehouse/changing-maintenance-schedule)<br>
* [Connect and manage your Data Warehouse using the Azure portal](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-portal)<br>
* [Connect and manage your Data Warehouse using PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-powershell)
