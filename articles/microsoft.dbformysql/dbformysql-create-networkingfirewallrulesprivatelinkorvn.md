<properties
    pageTitle="Networking in Azure Databases for MySQL"
    description="Networking in Azure Databases for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="540"
    selfHelpType="generic"
    supportTopicIds="32640056"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e6e54fce-02ca-44ae-b17e-9ff1bf769d87"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Networking in Azure Databases for MySQL

Azure Database for MySQL offers two deployment types - single server and flexible server. The networking options are available as per the deployment type.

Please refer to recommended steps for respective section for resolving common issues.

## **Recommended Steps**

### Azure Database for MySQL Flexible Server Networking

### Private access (VNet Integration)

* Learn how to enable private access (vnet integration) using the [Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-portal) or [Azure CLI](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-cli)
* You can deploy your flexible server into a virtual network and subnet during server creation. After the flexible server is deployed, you cannot move it into another virtual network, subnet or to *Public access (allowed IP addresses)*.
* The virtual network and subnet should be in the same region and subscription as your flexible server

### Public access (allowed IP addresses)

* Make sure you have the right [firewall settings](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-networking#firewall-rules) in place to allow the desired access to your server. You can either specify a single IP addresses or a range of IP addresses that are allowed to access your server.
* Public access (allowed IP addresses) can be managed through the [Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-portal) and the [Azure CLI](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-cli)

### Azure Database for MySQL Single Server Networking

### Private Link

* If you are using Private Link ensure the correct configuration of the [Private link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* If you are using a Basic tier server, note that [Private Link](https://docs.microsoft.com/azure/mysql/concepts-data-access-security-private-link) is not supported

### VNet Service endpoint

* If you are using VNets ensure the correct configuration of the [service endpoints](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal)
* If you are using a Basic tier server, note that VNet service endpoints is not supported

### Firewall rules

* To set up firewall rules on your client for outbound connection to Azure Database for MySQL Single Server, whitelist the gateway IP for your particular region. For information related to gateway IP addresses, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture#azure-database-for-mysql-gateway-ip-addresses)
* Make sure you have the right [firewall settings](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules) in place to allow the desired access to your server. You can either specify a single IP addresses or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/mysql/)
* If you are trying to connect to your server from other azure PaaS offerings, you must toggle the **Allow access to Azure services** option to *on*
* If the server's IP appears to be public and you can ping or connect using telnet, connections to the Azure Database for MySQL Single Server are routed through a publicly accessible Azure gateway. However, the actual server IP is protected by the firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture)

## **Recommended Documents**

* [Azure database for MySQL Flexible Server Networking overview](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-networking)
* Learn how to [connect using TLS/SSL to flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-connect-tls-ssl)
* [Create and manage Private Link for Azure Database for MySQL Single Server using Portal](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* [Configure a VNET connection for Azure Database for MySQL Single Server using Portal](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal/)
* [Firewall rule concepts in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules)