<properties
    pageTitle="VNET configuration for Azure Database for MySQL"
    description="Private Link for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    ms.author="jtoland"
    displayOrder="40"
    selfHelpType="generic"
    supportTopicIds="32788528"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="a362d3ee-e6cc-4f8b-8c58-22ab32e3462e"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# VNet configuration for Azure Database for MySQL

There are three networking options for accessing your Azure Database for MySQL Single Server instance:

* Private Link
* VNet service endpoints
* Firewall rules

To resolve common networking issues when working with Azure Database for MySQL Single Server, consider the following guidance.

## Fix it yourself

Refer to the appropriate section depending on your method of access.

### Troubleshooting issues with VNet service endpoints?

* Note that the **Basic** tier doesn’t support VNet service endpoints
* To ensure that VNet service endpoints are configured correctly, see [Create and manage VNet service endpoints and VNet rules](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal)

### Troubleshooting issues with Private Link?

* Note that the **Basic** tier doesn’t support [Private Link](https://docs.microsoft.com/azure/mysql/concepts-data-access-security-private-link)
* To ensure that Private Link is configured correctly, see [Create and manage Private Link using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* To configure an Azure Database for MySQL server to allow only connections through private endpoints, see [Deny public network access](https://docs.microsoft.com/azure/mysql/howto-deny-public-network-access)

### Troubleshooting issues with firewall rules?

* To ensure that you have the correct firewall settings to allow for appropriate access to your server, see [server firewall rules](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules). You can specify that either a single IP address or a range of IP addresses can access your server. To manage server-level firewall rules, you can use the [Azure portal](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-cli), or our [REST API](https://docs.microsoft.com/rest/api/mysql/).
* If you’re having issues with outbound connections from your client to the server, ensure that the gateway IP address for your particular region is included in the allow list. For additional detail on gateway IP addresses, see [Azure Database for MySQL gateway IP addresses](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture#azure-database-for-mysql-gateway-ip-addresses).
* If the server's IP address appears to be public and you can ping or connect using Telnet, connections to the server are routed through a publicly accessible Azure gateway. However, the actual IP address of the server is protected by the firewall. For more information, see [Connectivity architecture](https://docs.microsoft.com/azure/mysql/concepts-connectivity-architecture).
* If you’re having issues connecting to your server from other Azure PaaS offerings, ensure that the **Allow access to Azure services** option is set to **On**.

## Quick tips

Make sure to consider the following points.

* If you need to connect your server to Azure Kubernetes Services (AKS), see [Connecting Azure Kubernetes Service and Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-aks)
* If you're having issues connecting with SSL, see [Configure SSL connectivity in your application](https://docs.microsoft.com/azure/mysql/howto-configure-ssl)
* If you're having issues configuring TLS, see [Configuring TLS settings](https://docs.microsoft.com/azure/mysql/howto-tls-configurations)

## **Recommended documents**

* [Private Link for Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-data-access-security-private-link)
* [Create and manage Private Link for Azure Database for MySQL Single Server using Portal](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* [Configure a VNet connection using Azure portal](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal/)
* [Firewall rule concepts in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules)
* [Troubleshoot common connectivity issues to Azure Databases for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
* [Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal/)
