<properties
	pageTitle="Management|Scaling an instance"
	description="Management|Scaling an instance"
	service="microsoft.sql"
	resource="servers"
	authors="MladjoA"
    ms.author="mlandzic"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637303,32637304"
	productPesIds="16259"
	cloudEnvironments="public"
	articleId="46b0c74d-36e6-4a7f-9b62-f3bd8ee6962a"
	ownershipId="AzureData_AzureSQLMI"
/>

# Scaling an instance

Azure SQL Database provides management operations that you can use to automatically deploy new managed instances, update instance properties, and delete instances when no longer needed. All management operations can be categorized as follows:

- Instance deployment (new instance creation)
- Instance update (changing instance properties, such as vCores, reserved storage, pricing tier)
- Instance deletion

Instance update (scaling an instance) refers to scaling of vCores, storage capacity or pricing tier. Things to be aware of that are related to instance update are:

- Instance update is long running operation
- Instance update is not cancelable operation
- During instance update it is not possible to:

    - Run another update of same instance
    - Create, drop or restore databases
    - Alter database
    - Add/remove file

## **Recommended Steps**

If you are experiencing any issues or concerns related to scaling an instance:

- If issue is related to duration of instance scaling, read our [management operations duration](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations) article
- If issue is related to regional quota limits, read how to [submit quota increase request](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits#obtaining-a-larger-quota-for-sql-managed-instance)
- For list of API, PowerShell or CLI commands, check documentation page with [list of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)

## **Recommended Documents**

- [Managed Instance management operations duration](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations)
- [Quota increase request](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits#obtaining-a-larger-quota-for-sql-managed-instance)
- [List of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)
- [Dynamically scale resources with a minimal downtime](https://docs.microsoft.com/azure/sql-database/sql-database-scale-resources)
