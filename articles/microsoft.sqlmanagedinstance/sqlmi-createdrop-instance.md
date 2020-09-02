<properties
  pagetitle="Create or drop instance"
  service="microsoft.sql"
  resource="managedinstances"
  ms.author="katmac"
  selfhelptype="Generic"
  supporttopicids="32637269"
  resourcetags=""
  productpesids="16259"
  cloudenvironments="public,blackforest,fairfax,mooncake,ussec,usnat"
  articleid="f853015d-28f1-454e-9b08-154a60669a7c"
  ownershipid="AzureData_AzureSQLMI" />
# Create or drop instance

Provisioning a Microsoft Azure SQL Managed Instance can be accomplished using Azure Portal, PowerShell, CLI, or ARM templates. Before you begin, please be aware that:

- Creating an instance is a long-running operation
- Creating an instance is not a cancelable operation; once the operation begins, it must complete
- Managed instances are not available to client applications during deployment and deletion operations

## **Recommended Steps**

### Prepare Your Environment for the Creation of a Managed Instance

- Ensure that you have enough IP addresses to create an instance or scale within the subnet. Managed instances placed in a subnet with 16 IP addresses (the minimum number required) are not able to perform scaling operations so it is always recommended that you determine proper subnet size before deploying the managed instance. For more information, see the article [Determine required subnet size & range for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-subnet-determine-size).
- Decide when you want to create your new virtual network and subnet beforehand. They can be created before you begin creating the managed instance or while you create the managed instance. Refer to this topic if you decide to create the virtual network and subnet beforehand: [Create a virtual network for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/virtual-network-subnet-create-arm-template).
- If you already have a virtual network where you want to provision the managed instance, see [Configure an existing virtual network for Azure SQL Database Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-configure-vnet-subnet)

### Managed Instance Is Not Available for the Selected Subscription and Region

- Different subscription types have different resources available to them including regional deployments, and number of vCores or subnets available. More information can be found in [Supported subscription types](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits#supported-subscription-types). These limitations can be removed by submitting a quota increase request following the instructions in [this article](https://docs.microsoft.com/azure/sql-database/quota-increase-request#sqlmiquota).

### Delete Managed Instance Resources

- Managed instances can be deleted at any time. Deleted instances can't be restored
- To delete a virtual cluster, it needs to be empty; it should not contain any managed instances
- For instructions on how to delete a subnet and virtual cluster, see [Delete a subnet and virtual network](https://docs.microsoft.com/azure/azure-sql/managed-instance/virtual-cluster-delete)

### Create or Drop Databases in a Managed Instance

- Use the [Azure Portal](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-get-started#sign-in-to-the-azure-portal) to create or delete a managed instance
- For a list of API, PowerShell or CLI commands, see the [list of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)
- For information on how long it may take to create a managed instance, see [management operations duration](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations)
- Use ARM templates, see [Creating Azure SQL Managed Instance using ARM templates](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Creating-Azure-SQL-Managed-Instance-using-ARM-templates/ba-p/386203)

## **Recommended Documents**

- [Getting started with Azure SQL Database managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-quickstart-guide)
- [Managed Instance management operations duration](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations)
- [Quota increase request](https://docs.microsoft.com/azure/sql-database/quota-increase-request#sqlmiquota)
- [List of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)