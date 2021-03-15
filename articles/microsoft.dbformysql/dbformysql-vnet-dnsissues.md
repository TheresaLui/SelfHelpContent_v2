<properties
    pageTitle="Unable to connect to Azure Database for MySQL due to DNS issues"
    description="Unable to connect to Azure Database for MySQL due to DNS issues"
    service="microsoft.dbformysql"
    resource="servers"
    ms.author="jtoland"
    displayOrder="40"
    selfHelpType="generic"
    supportTopicIds="32788510"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6226f26d-ad37-4330-8054-ba63a9ee4bf7"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Unable to connect to Azure Database for MySQL due to DNS issues

With Azure Database for MySQL, you must correctly configure your DNS settings so that the private endpoint IP address resolves to the fully qualified domain name (FQDN) of the connection string. Existing Microsoft Azure services might already have a DNS configuration for a public endpoint, and connecting using your private endpoint requires overriding this configuration.

The network interface associated with the private endpoint contains the information you need to configure your DNS. The network interface information includes the FQDN and private IP addresses for your Private Link resource. For more information, see [Azure Private Endpoint DNS configuration](https://docs.microsoft.com/azure/private-link/private-endpoint-dns).

Be sure to use the predefined private DNS zone for your service, or to provide your preferred DNS zone name. For more information, see [Azure services DNS zone configuration](https://docs.microsoft.com/azure/private-link/private-endpoint-dns).

The FQDN in the customer DNS setting does not resolve to the private IP configured. You'll have to set up a DNS zone for the configured FQDN as described in [Manage DNS records and record sets](https://docs.microsoft.com/azure/dns/dns-operations-recordsets-portal).

## Fix it yourself

Refer to the appropriate section depending on the issues you're encountering.

### Troubleshooting issues with Private Link?

* Note that the **Basic** tier doesn’t support [Private Link](https://docs.microsoft.com/azure/mysql/concepts-data-access-security-private-link)
* To ensure that Private Link is configured correctly, see [Create and manage Private Link using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* To configure an Azure Database for MySQL server to allow only connections through private endpoints, see [Deny public network access](https://docs.microsoft.com/azure/mysql/howto-deny-public-network-access)

### Troubleshooting issues with VNet service endpoints?

* Note that the **Basic** tier doesn’t support VNet service endpoints
* To ensure that VNet service endpoints are configured correctly, see [Create and manage VNet service endpoints and VNet rules](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal)

## **Recommended documents**

* [Private Link for Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-data-access-security-private-link)
* [Create and manage Private Link for Azure Database for MySQL Single Server using Portal](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* [Configure a VNet connection using Portal](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal/)
* [Firewall rule concepts in Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/concepts-firewall-rules)
* [Troubleshoot common connectivity issues to Azure Databases for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
* [Connecting to MySQL Database: Best Practices and Design Guidelines](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal/)
