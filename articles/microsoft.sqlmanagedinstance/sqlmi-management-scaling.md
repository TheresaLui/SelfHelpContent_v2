<properties
  pagetitle="Scaling an instance"
  service="microsoft.sql"
  resource="managedinstances"
  ms.author="mlandzic,katmac"
  selfhelptype="Generic"
  supporttopicids="32637303,32637304"
  resourcetags=""
  productpesids="16259"
  cloudenvironments="public,blackforest,fairfax,mooncake,ussec,usnat"
  articleid="46b0c74d-36e6-4a7f-9b62-f3bd8ee6962a"
  ownershipid="AzureData_AzureSQLMI" />
# Scaling an instance

## **Recommended Steps**

**Scale Managed Instance Resources**

Scaling managed instance resources refers to the scaling of vCores, storage capacity, and service tiers. During managed instance scaling, it is NOT possible to:

- Run another update on the same managed instance
- Create, drop, or restore databases
- Alter a database
- Add or remove files

**Unable to Perform Scaling Operations**
- Managed instances placed in a subnet with 16 IP addresses (the minimum vNet size) are not able to perform scaling operations. See the [Determine vNet subnet size for Azure SQL Database Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-determine-size-vnet-subnet) article.
- To workaround the issue, create a new managed instance in a larger subnet, and then perform a [cross-instance point-in-time restore](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-point-in-time-restore) to the new managed instance

**Cancel a Scaling Operation**
- See the article [Cancel management operations](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#canceling-management-operations)

**Change the Hardware Generation of Scaling vCores**
- Changing the hardware generation by scaling vCores can be done using the Azure portal, PowerShell, or Azure CLI command. Storage size is determined by the vCore configuration. For more details, see the [Change the hardware generation of an existing managed instance](https://docs.microsoft.com/azure/sql-database/sql-database-service-tiers-vcore?tabs=azure-portal#selecting-a-hardware-generation) article. 

**Verify the Duration of a Scaling Operation**
- Scaling a managed instance is a long running operation. For more details about the duration of scaling operations, see [Managed instance management operations](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance#managed-instance-management-operations).

**Update Managed Instance Properties**
- To change public endpoint properties, see [Configure public endpoint in Azure SQL Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-public-endpoint-configure)
- The time zone can be set only during the managed instance creation and cannot be updated. For a workaround, see the [managed instance time zone FAQ section](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-faq#change-time-zone).
 
**Increase Quota Limits**
- Read how to [submit a quota increase request](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits#obtaining-a-larger-quota-for-sql-managed-instance)

**Find a List of Available Commands**
- For a list of API, PowerShell or CLI commands, see the article: [list of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)

## **Recommended Documents**

- [Quota increase request](https://docs.microsoft.com/azure/sql-database/quota-increase-request#sqlmiquota)
- [List of available commands](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-create-manage)
- [Dynamically scale resources with a minimal downtime](https://docs.microsoft.com/azure/sql-database/sql-database-scale-resources)
