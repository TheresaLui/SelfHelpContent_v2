<properties
    pageTitle="How to questions: Network settings"
    description="How to questions: Network settings"
    service="microsoft.sql"
    resource="managedinstances"
    authors="vitomaz-msft"
    ms.author="vitomaz"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32746115"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax,usnat,ussec,mooncake"
    resourceTags=""
    articleId="sqlmi-conn-config-networking"
    ownershipId="AzureData_AzureSQLMI"
/>

# How to questions: Network settings

**Network Settings**: Some connectivity settings are accessible from SQL Managed Instance > Networking, and configuring will apply to all databases in the managed instance.

 - **Public Endpoint** - Use to enable data access for clients outside of the connected virtual networks. Public endpoint will always default to Proxy connection mode. Learn how to [configure public endpoint](https://docs.microsoft.com/azure/azure-sql/managed-instance/public-endpoint-configure) or [use Azure SQL Managed Instance securely with public endpoints](https://docs.microsoft.com/azure/azure-sql/managed-instance/public-endpoint-overview).

 - **TLS Version** - The minimal TLS version enforced by the managed instance for inbound connections. Visit [configure minimal TLS version in Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/minimal-tls-version-configure) for commands to set the TLS version or if you have further questions or concerns.

 - **Connection Type** (private endpoint) - Azure SQL Managed Instance supports the following two connection types:

    - Redirect (recommended): Clients establish connections directly to the node hosting the database. To enable connectivity using redirect, you must open firewalls and Network Security Groups (NSG) to allow access on ports 1433, and 11000-11999. Packets go directly to the database, and hence there are latency and throughput performance improvements using redirect over proxy.

    - Proxy (default): In this mode, all connections are using a proxy gateway component. To enable connectivity, only port 1433 for private networks and port 3342 for public connection need to be opened. Choosing this mode can result in higher latency and lower throughput, depending on nature of the workload. We highly recommend the redirect connection policy over the proxy connection policy for the lowest latency and highest throughput.
 
**TCP Ports**: Port 1433 for private networks and port 3342 for public connection are the only ports that must be open on your computer that hosts the client application to SQL Managed Instance, when you are connecting using **Proxy** connection type. However, to make connections using **Redirect** connection type 
you must additionally open firewalls and Network Security Groups (NSG) to allow access on ports 11000-11999 as well.

**Firewalls**: Azure SQL Managed Instance does not have IP-based firewall like Azure SQL Database. The access to SQL Managed Instance is controlled via Network Security Groups (NSG). See [allow public endpoint traffic on the network security group](https://docs.microsoft.com/azure/azure-sql/managed-instance/public-endpoint-configure#allow-public-endpoint-traffic-on-the-network-security-group) for an example on how to add rules to a NSG.

## **Recommended Documents**

- [Connectivity architecture for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/connectivity-architecture-overview)
