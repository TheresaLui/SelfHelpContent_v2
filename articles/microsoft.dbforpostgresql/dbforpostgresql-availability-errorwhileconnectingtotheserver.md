<properties
    pageTitle="Connection issues to PostgreSQL"
    description="Connection issues to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="sunilagarwal"
    ms.author="sunila"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32639977, 32780963"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="14dc0ce8-a36f-4736-bd56-48f33e04eddd"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# **Error while connecting to server**

## **Recommended Steps**

### **Scenario: Connection failures/timeout during peak hours**

This means your connection string is correct and you can connect successfully during regular hours. However, during peak hours you may experience either connection failures or time outs.

- Check your active connections as well as CPU/memory/IO usage percentage in the portal metrics tab. High utilization may lead to unavailable resources for a new connection. Consider upgrading your server if the resource is reaching 100%.
- Check the connection limit of your PostgreSQL server using [pricing tier](https://docs.microsoft.com/azure/postgresql/concepts-limits). Review the configured number of connections and the usage.
- If you receive the message "An existing connection was forcibly closed by the remote host", it indicates that your client closed the connection to the PostgreSQL server. Check your client timeout and idle connection settings. Learn more about [this error.](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/are-you-running-into-postgres-connection-issues-on-azure/ba-p/1994913).

### **Scenario: All connections are failing suddenly**

The cause may be an issue in Azure structure or maintenance activities.

- There may be a planned maintenance activity going on your database server. Check the **Resource Health** for the status. We recommend setting up [planned maintenance notifications](https://docs.microsoft.com/azure/postgresql/concepts-planned-maintenance-notification) to get advance notification of maintenance activity.
- If you think there is a regional outage, see [Overview of business continuity](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity) with Azure Database for PostgreSQL for steps to recover to a new region.

### **Scenario: Unable to connect to PostgreSQL Server**

There can be multiple reasons for failing to establish the connection. The following steps could help you resolve the issue:

#### **Check connection string and password**

- Make sure the user you are connecting with an account has the appropriate permission
- Confirm that the username you are passing ends with the correct server name/hostname field (usernames need to be passed as username@servername)
- Make sure the password is correct in all connections. If you have enabled connection throttling server parameter in the portal, the database service will temporarily throttle connections per IP if there are too many invalid password login failures.

#### **Check if Security Rules are set correctly**

- Check the firewall rules in the portal. The error "pg_hba.conf entry for host 'xxxx', user 'xxxx', database 'pxxxx', SSL.." indicates that a firewall rule is needed. Set up [firewall rules](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules?WT.mc_id=Portal-Microsoft_Azure_Support) to allow your client's IP address.
- Make sure that you use the correct [SSL configuration](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security?WT.mc_id=Portal-Microsoft_Azure_Support) and choose the right certificate.
- As part of our maintenance activity, we are working on changing out the gateway certificate used to connect to the server [using SSL](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security?WT.mc_id=Portal-Microsoft_Azure_Support). Refer to the steps to mitigate the issue in this article.
- Make sure that you use the correct [TLS configuration](https://docs.microsoft.com/azure/postgresql/howto-tls-configurations?WT.mc_id=Portal-Microsoft_Azure_Support)

### **Check if client configuration is set correctly**

- You can simply test the connection from Azure CLI in the portal and see if you can connect. This test can help narrow down if the database is having an availability issue or a client network issue.
- Ping the FQDN and see if it resolves to our [Gateway IP](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture?WT.mc_id=Portal-Microsoft_Azure_Support) correctly. If you're using the private endpoint, it should resolve to your private IP for the private endpoint.
- Confirm that your network allows outbound connections on port 5432. You can try to telnet to your server. Confirm your network/firewall does not block connection to the regional Azure Database for PostgreSQL Gateway IP.
- If you're connecting within Azure VM (virtual machines), check NSG (network security groups) rules to see if it blocks the connection. Also check the route table and see if there is any VPN device which may need to be configured.
- If you're using VNET rules, ensure that the [service endpoints](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal?WT.mc_id=Portal-Microsoft_Azure_Support) are correctly configured.
- If you're using basic tier and see the error "Server is not configured to allow IPv6 connections", note that the Basic tier does not support VNet service endpoints. You must remove the endpoint Microsoft.Sql from the subnet attempting to connect to the Basic tier server.

#### **Check if you are using the right connection drivers?**

- Check out this supported [client library](https://docs.microsoft.com/azure/postgresql/concepts-connection-libraries) list.
- If you see an error related to GSS, you are likely using a newer client/driver version which Azure PostgreSQL Single Server does not yet fully support. This error is known to affect [JDBC driver versions 42.2.15 and 42.2.16](https://github.com/pgjdbc/pgjdbc/issues/1868).  Consider using a later driver version. Or, consider disabling the request of GSSAPI. Use a connection parameter like `gssEncMode=disable`.

### **Scenario: Connection is taking longer time**

The Single Server architecture leads to high connection time. This can impact your workload performance if there are large short duration connections. For example, user creates a connection, runs a simple query, and closes the connection. We highly recommend connection pooling if you have not done it yet and exam your pool configuration. [Learn more about this](https://azure.microsoft.com/blog/performance-best-practices-for-using-azure-database-for-postgresql-connection-pooling/).

If you notice the connection latency suddenly increases, you can start checking if you have increased workload.

## **Recommended Documents**

- [Troubleshoot common connectivity issues to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)
- [Tutorial: Creating and connecting to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
- [Understanding the connectivity architecture for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture)
