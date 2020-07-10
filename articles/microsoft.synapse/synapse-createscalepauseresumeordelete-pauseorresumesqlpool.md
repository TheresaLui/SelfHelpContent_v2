<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "sqlPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738785"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "Create, Scale, Pause, Resume or Delete/Pause or Resume SQL pool"
	description = "Create, Scale, Pause, Resume or Delete/Pause or Resume SQL pool"
	articleId = "synapse-createscalepauseresumeordelete-pauseorresumesqlpool"
	authors = "saltug"
	ms.author = "saltug"
/>

# Create, Scale, Pause, Resume or Delete/Pause or Resume SQL pool

## **Recommended Steps**

Resource Health determines the health of your SQL resource by examining the success and failure of logins to the resource every 1-2 minutes. A status of Unavailable means that Resource Health has detected consistent login failures due to system error on your SQL Database. A status of Degraded means that Resource Health has detected a majority of successful logins, but some failures as well. These login failures may be caused by transient errors.

* Check [Microsoft Azure Service Dashboard](https://azure.microsoft.com/status/) for any known issues
* Check [Resource Health](https://docs.microsoft.com/azure/service-health/resource-health-overview) blade in the Azure Portal for status updates. When available, downtime reasons for health events are reported in the Health History section of Resource Health. Downtime reasons are typically published 30 minutes after an event.
* Use the [available PowerShell commands](https://docs.microsoft.com/powershell/module/azurerm.sql/?view=azurermps-6.3.0#sql)
* Implementing [retry logic](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues#retry-logic-for-transient-errors) in your client application helps mitigate these situations and should generally make the errors transparent to the end user

## **Recommended Documents**

* [Troubleshooting connectivity issues](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity)
* [Additional Troubleshooting](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-troubleshoot/)
* [View maintenance schedule](https://docs.microsoft.com/azure/sql-data-warehouse/viewing-maintenance-schedule)
* [Connect and manage your Data Warehouse using the Azure portal](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-portal)
* [Connect and manage your Data Warehouse using PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-powershell)
* [Pause and resume from Azure portal](https://docs.microsoft.com/azure/sql-data-warehouse/pause-and-resume-compute-portal)
* [Pause and resume from PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/pause-and-resume-compute-powershell)
* [Manage compute](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-manage-compute-overview)
* [Scale from Azure portal](https://docs.microsoft.com/azure/sql-data-warehouse/quickstart-scale-compute-portal)
* [Scale from PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/quickstart-scale-compute-powershell)
* [Scale from T-SQL](https://docs.microsoft.com/azure/sql-data-warehouse/quickstart-scale-compute-tsql)


