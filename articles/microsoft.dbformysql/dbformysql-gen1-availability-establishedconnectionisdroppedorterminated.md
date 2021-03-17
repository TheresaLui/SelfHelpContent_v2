<properties
    pageTitle="Connection issues for Azure Database for MySQL Flexible Server"
    description="Connection issues for Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="40"
    selfHelpType="generic"
    supportTopicIds="32747561"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="4c19b79f-072a-4b30-a3d3-0abc6610f8a9"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Dropped connections

A connection established to an Azure Database for MySQL Single server can be terminated for multiple reasons, including client connection timeouts, changes to the server configuration, network failures, server restarts, and so on. Please work through the following steps for a first level of troubleshooting your connection issue.

To resolve problems with dropped connections when working with Azure Database for MySQL Single Server, consider the following guidance.

## Fix it yourself

* **Troubleshooting high CPU utilization or other resource limits?**

  If you experience high utilization on the CPU, remember that the number of active connections to your server can cause a spike. Be sure to review [Connecting efficiently to Azure Database for MySQL with ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842). For more information about resolving issues related to high CPU utilization and other resource limits, see [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815).

* **Troubleshooting high connection latency?**

  If you experience issues with high connection latency, review the details in [Connecting efficiently to Azure Database for MySQL with ProxySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/connecting-efficiently-to-azure-database-for-mysql-with-proxysql/ba-p/1279842).

  Also, consider connecting with redirection, which can reduce network latency between client applications and MySQL servers by allowing applications to connect directly to backend server nodes. For more information, see [Connect to Azure Database for MySQL with redirection](https://docs.microsoft.com/azure/mysql/howto-redirection). 

  You also might encounter "ERROR 2013: Lost connection to MySQL server during query"---a common error for MySQL databases. To resolve this issue, increase the value of the following parameters: `max_allowed_packet`, `connect_timeout`, `net_write_timeout`, `net_read_timeout`, and `wait_timeout`. This error can also result if resource usage on your server is very high. For more information, see [Azure Database for MySQL Performance Troubleshooting Basics](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/azure-database-for-mysql-performance-troubleshooting-basics/ba-p/782815).

  If you encounter the error "Azure Database for MySQL server has gone away", see [MySQL has gone away](https://techcommunity.microsoft.com/t5/azure-database-support-blog/azure-database-for-mysql-server-has-gone-away/ba-p/369138) troubleshooting guide.

  High connection latency can also result from a user configuration error. For potential issues with:

  * SSL, see [Configure SSL connectivity in your application to securely connect to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-configure-ssl).
  * VNet service endpoints and rules, see [Create and manage Azure Database for MySQL VNet service endpoints and VNet rules](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal).

  Finally, make sure that your server is not undergoing planned maintenance. For more information, see [Planned maintenance notification in Azure Database for MySQL - Single Server](https://docs.microsoft.com/azure/mysql/concepts-planned-maintenance-notification).

## Quick tips

Make sure to consider the following points:

* Try to reconnect to your server. If you can reconnect, switch the problem subtype to **Error while connecting to server** to help troubleshoot intermittent connection problems.
* Check the **Resource health** for your server to determine if there are any reported events that may have caused the connection disruption.
* Check the **Activity log** for your server to determine if there are server changes that may have caused the connection drops.
* Check your client logs to determine if you are experiencing connection timeouts or query timeouts. If so, then review your client's timeout settings.

## **Recommended documents**

* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
* [Tutorial: Creating and connecting to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal)
