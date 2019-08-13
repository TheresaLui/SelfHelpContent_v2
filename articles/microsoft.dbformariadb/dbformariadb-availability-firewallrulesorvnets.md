<properties
    pageTitle="Connection issues to MariaDB"
    description="Connection issues to MariaDB"
    service="microsoft.dbformariadb"
    resource="servers, databases"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="50"
    selfHelpType="generic"
    supportTopicIds="32640123"
    productPesIds="16617"
    cloudEnvironments="public"
    articleId="81e2e675-78c6-4d02-a363-a6c8f215c0c3"
/>

# Connection issues to Azure Databases for MariaDB

Firewall rules need to be configured to be able to access your Azure Database for MariaDB server.

## **Recommended Steps**

* Make sure you have the right [firewall settings](https://docs.microsoft.com/azure/mariadb/concepts-firewall-rules) in place by to allow the desired access to your server. You can either specify a single IP addresses or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-portal), the [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-cli), and our [REST API](https://docs.microsoft.com/rest/api/mariadb/).
* If you are using VNets ensure the correct configuration of the [service endpoints](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-portal)
* If you are trying to connect to your server from other azure PaaS offerings, you must toggle the **Allow access to Azure services** option to *on*
* If you are using a Basic tier server, note that VNet service endpoints are not supported

## **Recommended Documents**

* [Firewall rule concepts in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-firewall-rules)<br>
* [Use Virtual Network service endpoints and rules for Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-data-access-security-vnet/)<br>
* [Configure a VNET connection using Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-cli/)<br>
* [Configure a VNET connection using Portal](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-portal/)<br>
* [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MariaDB Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mariadb/tutorial-design-database-using-portal/)
