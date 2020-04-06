<properties
    pageTitle="Connection issues to PostgreSQL"
    description="Connection issues to PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32639977"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax"
    articleId="14dc0ce8-a36f-4736-bd56-48f33e04eddd"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Error while connecting to server

## **Recommended Steps**

### **Intermittent connection errors**
Causes of intermittent connection issues include server restart, high resource utilization on the server, and client timeouts. The following steps could help you resolve the issue:

* Retry the connection
* Check your server metrics to see if any resource is near 100% utilization. High utilization may lead to unavailable resources for a new connection.
* Check the [connections limit for your server's sku](https://docs.microsoft.com/azure/postgresql/concepts-limits)
* Check your client's timeout settings
* If the issue persists, see below:

### **Persistent connection errors**

If connection issues last for more than a couple minutes, the root cause may be a more persistent issue. Persistent connection issues when connecting to Azure Databases for PostgreSQL can occur due to an incorrect firewall configuration, an incorrect connection string, an incorrect virtual network (VNet) configuration, missing permissions for the user that is trying to connect, and other reasons. Work through the recommended steps to ensure you are not hitting a misconfiguration issue.

* The error "pg_hba.conf entry for host 'xxxx', user 'xxxx', database 'pxxxx', SSL..." indicates that a firewall rule is needed. [Set up firewall rules](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules) to allow your client's IP address.
* Confirm that your network allows outbound connections on port 5432 and to the regional Azure Database for PostgreSQL [gateway IP](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture)
* If you are using VNets, ensure that the [service endpoints](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal) are correctly configured.
* If you see the error *Server is not configured to allow ipv6 connections*, note that the Basic tier does not support VNet service endpoints. You have to remove the endpoint Microsoft.Sql from the subnet attempting to connect to the Basic server.
* The error *An existing connection was forcibly closed by the remote host* is likely caused by your application using a stale connection. Review your application's connection and pool settings and use retry logic.
* Make sure the user you are connecting with has the appropriate permissions
* Confirm that the username field correlates correctly with the servername/hostname field
* Follow [connection recommendations](https://docs.microsoft.com/azure/postgresql/concepts-connection-libraries) on computers hosting your client programs
* Make sure you are using the correct [SSL configuration](https://docs.microsoft.com/azure/postgresql/concepts-ssl-connection-security)


## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)<br>
* [Tutorial: Creating and connecting to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
* [Understanding the connectivity architecture for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture)
