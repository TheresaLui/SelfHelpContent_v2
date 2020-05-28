<properties
	pageTitle="Create or Drop Resources/Databases"
	description="Create or Drop Resources/Databases"
    infoBubbleText="Create or Drop Resources/Databases"
	service="microsoft.sql"
	resource="servers"
	authors="danimir"
	ms.author="danil"
	displayOrder=""
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32637257"
    resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="d3dcb634-9a99-4235-867b-326a89997f02"
	ownershipId="AzureData_AzureSQLMI"
/>

# Create or drop databases

Databases on managed instance can be created or dropped using T-SQL, API, PowerShell or Azure Portal.

When database is in a [restoring state](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups), it cannot be dropped using T-SQL. If you need to drop a database while it is restoring (e.g. if it takes an excessive amount of time to restore), this would only be possible using PowerShell. See [Remove-AzSqlInstanceDatabase](https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancedatabase?view=azps-2.8.0#examples) for an example.

## **Recommended Steps**

To create or drop databases on Managed Instance, consider following options:

* Use Azure Portal to create or delete databases
* Use client tools such is SSMS to connect to managed instance and execute T-SQL
* Invoke an API call, see [API documentation](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage#transact-sql-create-and-manage-instance-databases)
* Use PowerShell scripts, see [Azure.Rm PowerShell library](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Create-database-on-Azure-SQL-Managed-Instance-using-Azure-Rm/ba-p/386207)

## **Recommended Documents**

* [Getting started with Azure SQL Database managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-quickstart-guide)
