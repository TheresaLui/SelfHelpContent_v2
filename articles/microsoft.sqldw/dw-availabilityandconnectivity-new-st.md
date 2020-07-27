<properties
	pageTitle="How to troubleshoot availability and connectivity issues"
	description="How to troubleshoot availability and connectivity issues"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	supportTopicIds="32635176, 32635206"
	productPesIds="15818"
	displayOrder="10"
	selfHelpType="resource"
	resourceTags="datawarehouse"
	articleId="dw-availabilityandconnectivity.md"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# How to troubleshoot availability and connectivity issues

The following details explain how to set up and update common access and permissions rules in Azure SQL Data Warehouse.

* Connect and manage your data warehouse through the [Azure portal](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-portal#create-a-data-warehouse)
* View the [available PowerShell commands](https://docs.microsoft.com/powershell/module/azurerm.sql/?view=azurermps-6.3.0#sql)

## **Recommended Steps**

Issues connecting to SQL Data Warehouse can occur due to a number of issues including incorrect firewall configuration, connection strings, or maintenance periods. If you are having issues with a client tool, please ensure you have the latest version of the tool and [review the documentation](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot#tools).

Persistent connection issues to Azure SQL Database can occur due to incorrect firewall configuration, incorrect connection string, and other causes. 

Resource Health determines the health of your SQL resource by examining the success and failure of logins to the resource every 1-2 minutes. A status of **Unavailable** means that Resource Health has detected consistent login failures due to system error on your SQL Database. A status of **Degraded** means that Resource Health has detected a majority of successful logins, but some failures as well. These login failures may be caused by transient errors.

* Check [Resource Health](https://docs.microsoft.com/azure/service-health/resource-health-overview) blade in the Azure Portal for status updates. When available, downtime reasons for health events are reported in the Health History section of Resource Health. Downtime reasons are typically published 30 minutes after an event.
* Check [Microsoft Azure Service Dashboard](https://azure.microsoft.com/status/) for any known issues
* Set up [firewall rules](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-portal#create-a-server-level-firewall-rule) to allow the client IP address
* See how to [find the connection string](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-connect-overview#find-your-server-name) from the portal
* [Configure Azure AD authentication](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?WT.mc_id=pid:13491:sid:32745423/)
* [Configure multi-factor authentication for Azure AD](https://docs.microsoft.com/azure/sql-database/sql-database-ssms-mfa-authentication-configure?WT.mc_id=pid:13491:sid:32745423/)
* Implementing [retry logic](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues#retry-logic-for-transient-errors) in your client application helps mitigate these situations and should generally make the errors transparent to the end user

## **Recommended Documents**

* [Troubleshooting connectivity issues](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity)<br>
* [Additional Troubleshooting](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-troubleshoot/)<br>
* [Create a server-level firewall rule](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-portal#create-a-server-level-firewall-rule)<br>
* [Use virtual network service endpoints](https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview?toc=/azure/sql-data-warehouse/toc.json)<br>
* [SQL Data Warehouse Cheat Sheet](https://docs.microsoft.com/azure/sql-data-warehouse/cheat-sheet)<br>
* [View maintenance schedule](https://docs.microsoft.com/azure/sql-data-warehouse/viewing-maintenance-schedule)<br>
* [Change maintenance schedule](https://docs.microsoft.com/azure/sql-data-warehouse/changing-maintenance-schedule)<br>
* [Connect and manage your Data Warehouse using the Azure portal](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-portal)<br>
* [Connect and manage your Data Warehouse using PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-powershell)
