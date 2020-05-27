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
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="f853015d-28f1-454e-9b08-154a60669a7c"
	ownershipId="AzureData_AzureSQLMI"
/>

# Create or drop instance

Provisioning of managed instances can be managed using Azure Portal, PowerShell, CLI or ARM templates. Things to be aware of that are related to instance creation are:

- Creating instance is long running operation
- Creating instance is not cancelable operation
- Managed instances are not available to client applications during deployment and deletion operations

### Preparing environment for managed instance creation

- Sufficient number of IP addresses is required to execute instance creation or scaling inside subnet. Instances placed in subnet with 16 IP addresses (which is the bare minimum) are not able to perform scaling operations so it is always reocmmended to determine proper subnet size before deploying instance. For more details check: [Determine VNet subnet size for Azure SQL Database Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-determine-size-vnet-subnet)
- New Vnet and subnet can be create during managed instance creation, but in case you want to create it uprfront, check [Create a virtual network for Azure SQL Database Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-vnet-subnet)
- If you already have virtual network where you want to provision managed instance, check [Configure an existing virtual network for Azure SQL Database Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-configure-vnet-subnet) article


### What if I get message "Managed Instance is not available for the selected subscription and region."?

There are resource limitations based on subscription type including regional deployments, number of vCores or subnets available. More details can be found here: [Supported subscription types](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits#supported-subscription-types). This limitations can be removed by submitting quota requests following instructions from [this article](https://docs.microsoft.com/azure/sql-database/quota-increase-request#sqlmiquota)

### Deleting managed instance resources

- Managed instance can be deleted at any time and this action is not revertable. Deleted instances can't be restored.
- In order to delete Virtual Cluster it needs to be empty (no managed instances inside it)
- For instructions how to delete subnet and virtual cluster check [Delete a subnet after deleting an Azure SQL Database managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-delete-virtual-cluster) article

## **Recommended Steps**

To create or drop databases on Managed Instance, consider the following options:

- Use [Azure Portal](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-get-started#sign-in-to-the-azure-portal) to create or delete Managed Instances
- For list of API, PowerShell or CLI commands, check documentation page with [list of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)
- For info on duration of creating instance read our [management operations duration](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations) article
- Use ARM templates, see [Creating Azure SQL Managed Instance using ARM templates](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Creating-Azure-SQL-Managed-Instance-using-ARM-templates/ba-p/386203)

## **Recommended Documents**

- [Getting started with Azure SQL Database managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-quickstart-guide)
- [Managed Instance management operations duration](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations)
- [Quota increase request](https://docs.microsoft.com/azure/sql-database/quota-increase-request#sqlmiquota)
- [List of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)
