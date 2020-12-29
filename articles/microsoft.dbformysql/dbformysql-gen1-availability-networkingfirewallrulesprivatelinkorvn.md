<properties
    pageTitle="Networking in Azure Databases for MySQL - Single Server"
    description="Networking in Azure Databases for MySQL - Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="40"
    selfHelpType="generic"
    supportTopicIds="32747573"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="44456ad4-5e1d-42ba-9c39-0727277096ff"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Networking in Azure Databases for MySQL - Single Server

There are three networking option to access your Azure Database for MySQL Single Server:

* Private Link
* VNet Service endpoints
* Firewall rules

Please refer to recommended steps for respective section for resolving common issues.

## **Recommended Steps**

### Private Link

* If you are using Private Link ensure the correct configuration of the [Private link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* If you are using a Basic tier server, note that [Private Link](https://docs.microsoft.com/azure/mysql/concepts-data-access-security-private-link) is not supported

### VNet Service endpoint

* If you are using VNets ensure the correct configuration of the [service endpoints](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal)
* If you are using a Basic tier server, note that VNet service endpoints is not supported

### Firewall rules

* To set up firewall rules on your client for outbound connection to Azure Database for MySQL Single Server, whitelist the gateway IP for your particular region. For information related to gateway IP addresses, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture#azure-database-for-mysql-gateway-ip-addresses).
* Make sure you have the right [firewall settings](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules) in place to allow the desired access to your server. You can either specify a single IP addresses or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/mysql/).
* If you are trying to connect to your server from other azure PaaS offerings, you must toggle the **Allow access to Azure services** option to *on*
* If the server's IP appears to be public and you can ping or connect using telnet, connections to the Azure Database for MySQL Single Server are routed through a publicly accessible Azure gateway. However, the actual server IP is protected by the firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture).

## **Recommended Documents**

* [Create and manage Private Link for Azure Database for MySQL Single Server using Portal](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* [Configure a VNET connection using Portal](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal/)<br>
* [Firewall rule concepts in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules)<br>
* [Troubleshoot common connectivity issues to Azure Databases for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)<br>
* [Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal/)