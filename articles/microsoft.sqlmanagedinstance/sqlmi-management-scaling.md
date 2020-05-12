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
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="46b0c74d-36e6-4a7f-9b62-f3bd8ee6962a"
	ownershipId="AzureData_AzureSQLMI"
/>

# Scaling an instance

## Scaling instance resources

Scaling an instance resources refers to scaling of vCores, storage capacity or pricing tier. Things to be aware of that are related to instance update are:

- Sufficient number of IP addresses is required to execute instance scaling. Instances placed in subnet with 16 IP addresses (which is the bare minimum) are not able to perform scaling operations, For more details check: [Determine VNet subnet size for Azure SQL Database Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-determine-size-vnet-subnet). The workaround is creating new instance in larger subnet then perform a [cross-instance point-in-time restore](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-point-in-time-restore).
- Changing hardware generation, scaling vCores or storage can be done using Azure Portal, PowerShell or Azure CLI command. For more details check: [Change the hardware generation of an existing managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-vcore?tabs=azure-portal#selecting-a-hardware-generation)
- Maximum storage available is dependent on number of vCores consumed. For more details check [Azure SQL Database managed instance resource limits article](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits)
- Scaling instance is long running operation. For more details about duration of scaling operations check: [Managed instance management operations](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations)
-Scaling an instance can be cancelled: [Cancel management operation](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#canceling-management-operations)
- During instance scaling it is not possible to:
    - Run another update of same instance
    - Create, drop or restore databases
    - Alter database
    - Add/remove file
    
## Updating instance properties

Updating instance properties refers to updating some of the instance properties:
- Public endpoint - read [how to configure public endpoint](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-public-endpoint-configure)
- Time zone - time zone can be set only during instance creation and can't be updated. For workaround, check our [managed instance time zone FAQ section](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-faq#change-time-zone)
 

## **Recommended Steps**

If you are experiencing any issues or concerns related to scaling an instance:

- If issue is related to duration of instance scaling, read our [management operations duration](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations) article
- If issue is related to regional quota limits, read how to [submit quota increase request](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits#obtaining-a-larger-quota-for-sql-managed-instance)
- For list of API, PowerShell or CLI commands, check documentation page with [list of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)

## **Recommended Documents**

- [Managed Instance management operations duration](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations)
- [Quota increase request](https://docs.microsoft.com/azure/sql-database/quota-increase-request#sqlmiquota)
- [List of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)
- [Dynamically scale resources with a minimal downtime](https://docs.microsoft.com/azure/sql-database/sql-database-scale-resources)
