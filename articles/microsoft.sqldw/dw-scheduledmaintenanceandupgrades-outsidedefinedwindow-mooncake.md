<properties
	pageTitle="How to manage and troubleshoot Scheduled Maintenance and upgrades"
	description="How to manage and troubleshoot Scheduled Maintenance and upgrades"
	service="microsoft.sql"
	resource="servers"
	authors="saltug,mlee3gsd"
	ms.author="saltug,martinle"
	supportTopicIds=""
	productPesIds=""
	displayOrder="15"
	selfHelpType="resource"
	resourceTags="datawarehouse"
	articleId="dw-scheduledmaintenanceandupgrades-outsidedefinedwindow-mooncake"
	cloudEnvironments="MoonCake"
	ownershipId="AzureData_AzureSQLDB"
/>

# How to manage and troubleshoot Scheduled Maintenance and upgrades

## **Recommended Steps**

By default, all newly created Azure SQL Data Warehouse instances have an eight-hour primary and secondary maintenance window applied during deployment. You can change the windows as soon deployment is complete. No maintenance will take place outside the specified maintenance windows without prior notification.

To view the maintenance schedule that has been applied to your data warehouse, complete the following steps:

1. Sign in to the [Azure portal](https://portal.azure.cn/)
2. Select the data warehouse that you want to view
3. The selected data warehouse opens on the overview blade

## **Recommended Documents**

* [Maintenance Schedules](https://docs.azure.cn/sql-data-warehouse/maintenance-scheduling)
* Check your [current Maintenance Schedule](https://docs.azure.cn/sql-data-warehouse/viewing-maintenance-schedule)