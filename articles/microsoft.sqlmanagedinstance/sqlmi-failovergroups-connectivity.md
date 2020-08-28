<properties
    pageTitle="Connectivity to geo-secondary database"
    description="Connectivity to geo-secondary database"
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
    articleId="sqlmi-failovergroups-configuring"
    ownershipId="AzureData_AzureSQLMI"
/>

# Connectivity to geo-secondary database

**Read-write and read-only listeners**

Read-write and read-only listeners are DNS CNAME records that points to the current primary's URL and secondary's URL. They are created automatically when the failover group is created and allows the workloads to transparently reconnect to the new primary/secondary when they changes after failover. 
- The DNS CNAME record for the read-write listener URL is formed as `<fog-name>.zone_id.database.windows.net`.
- The DNS CNAME record for the read-only listener URL is formed as `<fog-name>.zone_id.secondary.database.windows.net`.

In certain service tiers, SQL Managed Instance supports the use of [read-only replicas](https://docs.microsoft.com/azure/azure-sql/database/read-scale-out) to load balance read-only query workloads using the capacity of one read-only replica and using the `ApplicationIntent=ReadOnly` parameter in the connection string. When you have configured a geo-replicated secondary, you can use this capability to connect to either a read-only replica in the primary location or in the geo-replicated location.

- To connect to a read-only replica in the primary location, use `<fog-name>.zone_id.database.windows.net`.
- To connect to a read-only replica in the secondary location, use `<fog-name>.secondary.zone_id.database.windows.net`.

**Connectivity issues to geo secondary database** 

Connectivity issues can be caused by one or more of the possible scenarios**

- Transient errors - Azure infrastructure dynamically reconfigure servers when heavy workloads arise in the SQL Database service. This dynamic behavior might cause your client program to lose its connection to geo secondary database (Error 40613/40197) for a short window (transient faults). Database reconfiguration events occur because of a planned event (for example, a software upgrade) or an unplanned event (for example, a process crash, or load balancing). Most reconfiguration events are generally short-lived and should be completed in less than 60 seconds at most. However, these events can occasionally take longer to finish, such as when a large transaction causes a long-running recovery.

- Other common connectivity issues can be related to network, firewall configuration or user errors

## **Recommended Steps**

- [Troubleshooting connectivity issues and other errors with Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-errors-issues) 
- [Work with transient errors](https://docs.microsoft.com/azure/azure-sql/database/troubleshoot-common-connectivity-issues)