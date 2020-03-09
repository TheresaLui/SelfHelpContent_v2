<properties
	pageTitle="Create or Drop Resources/Instance"
	description="Create or Drop Resources/Instance"
    infoBubbleText="Create or Drop Resources/Instance"
	service="microsoft.sql"
	resource="servers"
	authors="danimir"
	ms.author="danil"
	displayOrder=""
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32637269"
    resourceTags=""	
	productPesIds="16259"
	cloudEnvironments="public"
	articleId="f853015d-28f1-454e-9b08-154a60669a7c"
	ownershipId="AzureData_AzureSQLMI"
/>

# Create or drop instance

Azure SQL Database provides management operations that you can use to automatically deploy new managed instances, update instance properties, and delete instances when no longer needed. All management operations can be categorized as follows:

- Instance deployment (new instance creation)
- Instance update (changing instance properties, such as vCores, reserved storage, pricing tier)
- Instance deletion

Provisioning of managed instances can be managed using Azure Portal, PowerShell, CLI or ARM templates. Things to be aware of that are related to instance creation are:

- Creating instance is long running operation
- Creating instance is not cancelable operation
- Managed instances are not available to client applications during deployment and deletion operations

## **Recommended Steps**

To create or drop databases on Managed Instance, consider the following options:

- Use [Azure Portal](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-get-started#sign-in-to-the-azure-portal) to create or delete Managed Instances
- For list of API, PowerShell or CLI commands, check documentation page with [list of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)
- For info on duration of creating instance read our [management operations duration](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations) article
- Use ARM templates, see [Creating Azure SQL Managed Instance using ARM templates](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Creating-Azure-SQL-Managed-Instance-using-ARM-templates/ba-p/386203)

## **Recommended Documents**

- [Getting started with Azure SQL Database managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-quickstart-guide)
- [Managed Instance management operations duration](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations)
- [Quota increase request](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits#obtaining-a-larger-quota-for-sql-managed-instance)
- [List of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)
