<properties
    pageTitle="Connection issues to MariaDB"
    description="Connection issues to MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32640118"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="bb62de23-25af-4ae3-9740-7a7670636337"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Connection issues to Azure Databases for MariaDB

Persistent connection issues when connecting to Azure Databases for MariaDB can occur due to an incorrect firewall configuration, an incorrect connection string, an incorrect VNet configuration, missing permissions for the user that is trying to connect, and others. Work through the recommended steps to ensure you are not hitting a misconfiguration problem.

## **Recommended Steps**

### **Intermittent connection errors**
Causes of intermittent connection issues include server restart, high resource utilization on the server, and client timeouts. The following steps could help you resolve the issue:

* Retry the connection
* Check your server metrics to see if any resource is near 100% utilization. High utilization may lead to unavailable resources for a new connection.
* Check your client's timeout settings
* If the issue persists, see below

### **Persistent connection errors**
If connection issues last for more than a couple minutes, the root cause may be a more persistent issue. Persistent connection issues when connecting to Azure Databases for MariaDB can occur due to an incorrect firewall configuration, an incorrect connection string, an incorrect virtual network (VNet) configuration, missing permissions for the user that is trying to connect, and other reasons. Work through the recommended steps to ensure you are not hitting a misconfiguration issue.

* [Set up firewall rules](https://docs.microsoft.com/azure/mariadb/concepts-firewall-rules) to allow your client's IP address
* If you are using VNets, ensure the correct configuration of the [service endpoints](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-portal). Note that the Basic tier does not support VNet service endpoints.
* Follow [connection recommendations](https://docs.microsoft.com/azure/mariadb/connect-workbench) on computers hosting your client programs
* Fix [incorrect connection strings](https://docs.microsoft.com/azure/mariadb/howto-connection-string) in your application
* Make sure you are using the correct [SSL configuration](https://docs.microsoft.com/azure/mariadb/howto-configure-ssl)
* As a part of our maintenance activity, we are working on changing out gateway certificate used to [connect to the server using SSL](https://docs.microsoft.com/azure/mariadb/concepts-ssl-connection-security#default-settings). Refer to the steps to mitigate the issue in [this article](https://docs.microsoft.com/azure/mariadb/concepts-certificate-rotation)
* Make sure you are using the correct [TLS configuration](https://docs.microsoft.com/azure/mariadb/howto-tls-configurations)
* Review the [supported client driver list](https://docs.microsoft.com/azure/mariadb/concepts-compatibility) and ensure you are using a driver that is supported
* Make sure the user you are using has the appropriate permissions

## **Recommended Documents**

*   [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)
*   [Connecting to MariaDB Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mariadb/tutorial-design-database-using-portal/)
*   [Understanding the connectivity architecture for Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-connectivity-architecture)