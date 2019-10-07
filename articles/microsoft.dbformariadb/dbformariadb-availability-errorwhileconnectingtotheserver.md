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
    cloudEnvironments="public"
    articleId="bb62de23-25af-4ae3-9740-7a7670636337"
/>

# Connection issues to Azure Databases for MariaDB

Persistent connection issues when connecting to Azure Databases for MariaDB can occur due to an incorrect firewall configuration, an incorrect connection string, an incorrect VNet configuration, missing permissions for the user that is trying to connect, and others. Work through the recommended steps to ensure you are not hitting a misconfiguration problem.

## **Recommended Steps**

* [Set up firewall rules](https://docs.microsoft.com/azure/mariadb/concepts-firewall-rules) to allow your client's IP address
* If you are using VNets, ensure the correct configuration of the [service endpoints](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-portal). Note that the Basic tier does not support VNet service endpoints.
* Follow [connection recommendations](https://docs.microsoft.com/azure/mariadb/connect-workbench) on computers hosting your client programs
* Fix [incorrect connection strings](https://docs.microsoft.com/azure/mariadb/howto-connection-string) in your application
* Make sure you are using the correct [SSL configuration](https://docs.microsoft.com/azure/mariadb/howto-configure-ssl)
* Review the [supported client driver list](https://docs.microsoft.com/azure/mariadb/concepts-compatibility) and ensure you are using a driver that is supported
* Make sure the user you are using has the appropriate permissions

## **Recommended Documents**

* [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MariaDB Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mariadb/tutorial-design-database-using-portal/)
