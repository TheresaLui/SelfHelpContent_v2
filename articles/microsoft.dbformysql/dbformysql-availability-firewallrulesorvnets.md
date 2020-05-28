<properties
    pageTitle="Connection issues to Azure Databases for MySQL"
    description="Connection issues to Azure Databases for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="50"
    selfHelpType="generic"
    supportTopicIds="32640058"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="1007778f-3183-495d-9184-a825b0fb0f5d"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Connection issues to Azure Databases for MySQL

Firewall rules need to be configured to be able to access your Azure Database for MySQL server.

## **Recommended Steps**

* To set up firewall rules on your client for outbound connection to Azure Database for MySQL, whitelist the gateway IP for your particular region. For information related to gateway IP addresses, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture#azure-database-for-mysql-gateway-ip-addresses).
* Make sure you have the right [firewall settings](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules) in place by to allow the desired access to your server. You can either specify a single IP addresses or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/mysql/).
* If you are using VNets ensure the correct configuration of the [service endpoints](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal)
* If you are using Private Link ensure the correct configuration of the [Private link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* If you are trying to connect to your server from other azure PaaS offerings, you must toggle the **Allow access to Azure services** option to *on*
* If you are using a Basic tier server, note that VNet service endpoints and [Private Link](https://docs.microsoft.com/azure/mysql/concepts-data-access-security-private-link) are not supported
* If the server's IP appears to be public and you can ping or connect using telnet, connections to the Azure Database for MySQL server are routed through a publicly accessible Azure gateway. However, the actual server IP is protected by the firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture).

## **Recommended Documents**

* [Firewall rule concepts in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules)<br>
* [Use Virtual Network service endpoints and rules for Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-data-access-and-security-vnet/)<br>
* [Configure a VNET connection using Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-cli/)<br>
* [Configure a VNET connection using Portal](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal/)<br>
* [Point to site connectivity using VNet service endpoints](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/secure-connectivity-from-on-premise-to-azure-database-for-mysql/ba-p/793905)<br>
* [Point to site connectivity using Private Link](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/using-private-link-and-point-to-site-gateway-for-secure-on/ba-p/1108953)<br>
* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal/)
