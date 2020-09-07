<properties
    pageTitle="Connection issues to MariaDB"
    description="Connection issues to MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="50"
    selfHelpType="generic"
    supportTopicIds="32640123"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="81e2e675-78c6-4d02-a363-a6c8f215c0c3"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Connection issues to Azure Databases for MariaDB

Firewall rules need to be configured to be able to access your Azure Database for MariaDB server.

## **Recommended Steps**

* To set up firewall rules on your client for outbound connection to Azure Database for MariaDB, whitelist the gateway IP for your particular region. For information related to gateway IP addresses, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mariadb/concepts-connectivity-architecture#azure-database-for-mariadb-gateway-ip-addresses).
* Make sure you have the right [firewall settings](https://docs.microsoft.com/azure/mariadb/concepts-firewall-rules) in place by to allow the desired access to your server. You can either specify a single IP addresses or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-portal), the [Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-firewall-cli), and our [REST API](https://docs.microsoft.com/rest/api/mariadb/).
* If you are using VNets ensure the correct configuration of the [service endpoints](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-portal)
* If you are using Private Link ensure the correct configuration of the [Private link](https://docs.microsoft.com/azure/mariadb/howto-configure-privatelink-portal)
* If you are trying to connect to your server from other azure PaaS offerings, you must toggle the **Allow access to Azure services** option to *on*
* If you are using a Basic tier server, note that VNet service endpoints and [Private Link](https://docs.microsoft.com/azure/mariadb/concepts-data-access-security-private-link) are not supported
* If the server's IP appears to be public and you can ping or connect using telnet, connections to the Azure Database for MariaDB server are routed through a publicly accessible Azure gateway. However, the actual server IP is protected by the firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mariadb/concepts-connectivity-architecture).

## **Recommended Documents**

* [Firewall rule concepts in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-firewall-rules)<br>
* [Use Virtual Network service endpoints and rules for Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-data-access-security-vnet/)<br>
* [Configure a VNET connection using Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-cli/)<br>
* [Configure a VNET connection using Portal](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-portal/)<br>
* [Point to site connectivity using VNet service endpoints](https://techcommunity.microsoft.com/t5/azure-database-for-mariadb/secure-connectivity-from-on-premise-to-azure-database-for/ba-p/1003983)<br>
* [Point to site connectivity using Private Link](https://techcommunity.microsoft.com/t5/azure-database-for-mariadb/using-private-link-and-point-to-site-gateway-for-secure-on/ba-p/1109010)<br>
* [Troubleshoot common connectivity issues to Azure Databases for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MariaDB Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mariadb/tutorial-design-database-using-portal/)
