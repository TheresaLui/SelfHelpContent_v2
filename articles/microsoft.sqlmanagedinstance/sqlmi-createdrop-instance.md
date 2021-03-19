<properties
  pagetitle="Create or drop instance"
  service="microsoft.sql"
  resource="managedinstances"
  ms.author="katmac,urmilano"
  selfhelptype="Generic"
  supporttopicids="32637269"
  resourcetags=""
  productpesids="16259"
  cloudenvironments="public,blackforest,fairfax,mooncake,ussec,usnat"
  articleid="f853015d-28f1-454e-9b08-154a60669a7c"
  ownershipid="AzureData_AzureSQLMI" />
# Create or drop instance

You can provision a Microsoft Azure SQL Managed Instance by using the Azure portal, PowerShell, CLI, or ARM templates. Before you begin, be aware that:

- Creating an instance is a [long-running operation](https://docs.microsoft.com/azure/azure-sql/managed-instance/management-operations-overview#duration)
- Managed instances are not available to client applications during deployment and deletion operations

## **Recommended Steps**

### Prepare your environment for the creation of a managed instance

- By design, a managed instance needs a minimum of 32 IP addresses in a subnet. Therefore, you can use minimum subnet mask of /27 when defining your subnet IP ranges. We recommend careful planning of subnet size for your managed instance deployments. For more information, see [Determine required subnet size & range for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/vnet-subnet-determine-size).
- Decide when you want to create your new virtual network and subnet beforehand. You can create them before you begin creating the managed instance or while you create the managed instance. If you decide to create the virtual network and subnet beforehand, see [Create a virtual network for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/virtual-network-subnet-create-arm-template).
- If you already have a virtual network where you want to provision the managed instance, see [Configure an existing virtual network for Azure SQL Database Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-configure-vnet-subnet)

### Create or drop managed instances

- Use the [Azure portal](https://docs.microsoft.com/azure/azure-sql/managed-instance/instance-create-quickstart) to create or delete a managed instance
- For a list of API, PowerShell or CLI commands, see the [list of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)
- For information regarding how long it will take to create a managed instance, see [management operations duration](https://docs.microsoft.com/azure/azure-sql/managed-instance/management-operations-overview#duration)
- For information on how to monitor management operations, see [Monitoring Azure SQL Managed Instance management operations](https://docs.microsoft.com/azure/azure-sql/managed-instance/management-operations-monitor)
- To use ARM templates, see the Quickstart: [Creating Azure SQL Managed Instance using ARM templates](https://docs.microsoft.com/azure/azure-sql/managed-instance/create-template-quickstart)

### Managed instance is not available for the selected subscription and region

- Different subscription types have different resources available to them, including regional deployments, and number of vCores or subnets available. For more information, see [Supported subscription types](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits#supported-subscription-types). You can remove these limitations by submitting a quota increase request. For instructions, see [this article](https://docs.microsoft.com/azure/sql-database/quota-increase-request#sqlmiquota).

### Canceling create request

The **Cancel** button on the **Resource group deployments** blade, [will not cancel an ongoing managed instance create request](https://docs.microsoft.com/azure/azure-sql/managed-instance/management-operations-monitor#overview). However, the managed instance create request can be canceled from the **Managed instance overview** blade. For detailed instructions, see [Canceling Azure SQL Managed Instance management operations](https://docs.microsoft.com/azure/azure-sql/managed-instance/management-operations-cancel).

### Delete managed instance resources

- Managed instances can be deleted at any time. Note, however, that deleted instances can't be restored.
- To delete a virtual cluster, the cluster must be empty. It should not contain any managed instances.
- For instructions on how to delete a subnet and virtual cluster, see [Delete a subnet and virtual network](https://docs.microsoft.com/azure/azure-sql/managed-instance/virtual-cluster-delete)

## **Recommended Documents**

- [Getting started with Azure SQL Database managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-quickstart-guide)
- [Managed Instance management operations overview](https://docs.microsoft.com/azure/azure-sql/managed-instance/management-operations-overview)
- [Quota increase request](https://docs.microsoft.com/azure/sql-database/quota-increase-request#sqlmiquota)
- [List of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)
