<properties
    pageTitle="Configuring or using failover groups"
    description="Configuring or using failover groups"
    service="microsoft.sql"
    resource="managedinstances"
    authors="vitomaz-msft"
    ms.author="vitomaz"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32748009"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags=""
    articleId="sqlmi-failovergroups-configuring"
    ownershipId="AzureData_AzureSQLMI"
/>

# Configuring or using failover groups

You can [use auto-failover groups to enable transparent and coordinated failover of multiple databases](https://docs.microsoft.com/azure/azure-sql/database/auto-failover-group-overview?tabs=azure-powershell) in Azure SQL Managed Instance.

The auto-failover group must be configured on the primary instance and will connect it to the secondary instance in a different Azure region. All databases in the instance will be replicated to the secondary instance.

## **Recommended Steps**

Before creating failover group(s), it is critical to consider the following prerequisites:

- The two instances of SQL Managed Instance need to be the same service tier, and have the same storage size
- Your secondary instance of SQL Managed Instance must be empty (no user databases)
- The virtual networks used by the instances of SQL Managed Instance need to be connected through a VPN Gateway or Express Route. When two virtual networks connect through an on-premises network, ensure there is no firewall rule blocking ports 5022, and 11000-11999. Global VNet Peering is not supported.
- The two SQL Managed Instance VNets cannot have overlapping IP addresses
- You need to set up your Network Security Groups (NSG) such that ports 5022 and the range 11000~12000 are open inbound and outbound for connections from the subnet of the other managed instance. This is to allow replication traffic between the instances. 
- The secondary SQL Managed Instance is configured with the same DNS zone ID as the primary

See [Add managed instance to a failover group](https://docs.microsoft.com/azure/azure-sql/managed-instance/failover-group-add-instance-tutorial?tabs=azure-portal) for a detailed step-by-step tutorial adding a SQL Managed Instance to use failover group using [Azure portal](https://docs.microsoft.com/azure/azure-sql/managed-instance/failover-group-add-instance-tutorial?tabs=azure-portal) or [PowerShell](https://docs.microsoft.com/azure/azure-sql/managed-instance/failover-group-add-instance-tutorial?tabs=azure-powershell).

- If the connection between primary and secondary Managed Instances cannot be established, check are the resources in secondary VNet reachable from the primary VNets. You would need to use express route or Gateway to connect the networks, and to remove any firewall rules that can block the traffic.
- If the VNets are connected check are you using [Global VNet peering](https://docs.microsoft.com/azure/virtual-network/virtual-networks-faq#what-are-the-constraints-related-to-global-vnet-peering-and-load-balancers). VNet peering is not supported in Geo-replication scenario and you need to use express route or Gateway to connect the VNets.

**Creating a failover group between managed instances in different subscriptions**

You can create a failover group between SQL Managed Instances in two different subscriptions, as long as subscriptions are associated to the same Azure Active Directory Tenant. Azure portal does not support the creation of failover groups across different subscriptions, use [PowerShell or REST API](https://docs.microsoft.com/azure/azure-sql/database/auto-failover-group-overview?tabs=azure-powershell#creating-a-failover-group-between-managed-instances-in-different-subscriptions).

**Managing failover to secondary instance**

The failover group will manage the failover of all the databases in the SQL Managed Instance. When a group is created, each database in the instance will be automatically geo-replicated to the secondary SQL Managed Instance. You cannot use failover groups to initiate a partial failover of a subset of the databases.

For the existing failover groups across different subscriptions and/or resource groups, failover cannot be initiated manually via portal from the primary SQL Managed Instance. Initiate it from the geo-secondary instance instead.

**Read-write and read-only listeners**

Read-write and read-only listeners are DNS CNAME records that points to the current primary's URL and secondary's URL. They are created automatically when the failover group is created and allows the workloads to transparently reconnect to the new primary/secondary when they changes after failover. 

- The DNS CNAME record for the read-write listener URL is formed as `<fog-name>.<zone_id>.database.windows.net`
- The DNS CNAME record for the read-only listener URL is formed as `<fog-name>.secondary.<zone_id>.database.windows.net`

## **Recommended Documents**

- [Best practices for configuring auto-failover group in Managed Instance](https://docs.microsoft.com/azure/azure-sql/database/auto-failover-group-overview?tabs=azure-powershell#best-practices-for-sql-managed-instance) 
- [Enabling geo-replication between managed instances and their VNets](https://docs.microsoft.com/azure/azure-sql/database/auto-failover-group-overview?tabs=azure-powershell#enabling-geo-replication-between-managed-instances-and-their-vnets)
