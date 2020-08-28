<properties
    pageTitle="Connectivity to geo-secondary instance"
    description="Connectivity to geo-secondary instance"
    service="microsoft.sql"
    resource="managedinstances"
    authors="vitomaz-msft"
    ms.author="vitomaz"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32748010"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags=""
    articleId="sqlmi-failovergroups-connectivity"
    ownershipId="AzureData_AzureSQLMI"
/>

# Connectivity to geo-secondary instance

**Read-write and read-only listeners**

Read-write and read-only listeners are DNS CNAME records that points to the current primary's URL and secondary's URL. They are created automatically when the failover group is created and allows the workloads to transparently reconnect to the new primary/secondary when they changes after failover. 

- The DNS CNAME record for the read-write listener URL is formed as `<fog-name>.<zone_id>.database.windows.net`
- The DNS CNAME record for the read-only listener URL is formed as `<fog-name>.secondary.<zone_id>.database.windows.net`

In certain service tiers, SQL Managed Instance supports the use of [read-only replicas](https://docs.microsoft.com/azure/azure-sql/database/read-scale-out) to load balance read-only query workloads using the capacity of one read-only replica and using the `ApplicationIntent=ReadOnly` parameter in the connection string. When you have configured a geo-replicated secondary, you can use this capability to connect to either a read-only replica in the primary location or in the geo-replicated location.

- To connect to a read-only replica in the primary location, use `<fog-name>.<zone_id>.database.windows.net`
- To connect to a read-only replica in the secondary location, use `<fog-name>.secondary.<zone_id>.database.windows.net`

**Connectivity issues to geo secondary database** 

Connectivity issues are usually associated with transient errors.

The Azure infrastructure has the ability to dynamically reconfigure servers for planned operations such as load balancing and updates, or unplanned occurrences such as recoveries from software or hardware issues. Most reconfiguration events take less than 60 seconds to complete. This behavior might cause your client program to lose its connection to geo secondary database (Error 40613/40197) for a short window (transient faults).  
   
Building resiliency into your application to account for these situations can help create transparency to the end user when these transient scenarios occur. For information about connectivity in Azure SQL, how to implement retry logic, and to understand common errors in Azure SQL please refer to this article on [database connection errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-errors-issues#database-connection-errors-transient-errors-and-other-temporary-errors). 

Other common connectivity issues can be related to network, firewall configuration or user errors.

## **Recommended Steps**

- [Troubleshooting connectivity issues and other errors with Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-errors-issues) 
- [Working with transient errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues)
