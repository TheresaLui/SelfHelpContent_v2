<properties
    pageTitle="Managing firewall rules for Azure Database for PostgreSQL"
    description="Managing firewall rules for Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="50"
    selfHelpType="generic"
    supportTopicIds="32639982"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="88983e2b-0ed3-4183-8eb3-24ecc5539e4e"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Managing firewall rules and virtual networks

[Firewall rules](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules) or [virtual network service endpoints](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet) need to be configured to enable access to your Azure Database for PostgreSQL server.

## **Recommended Steps**

* You can either specify a single IP address or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/postgresql/).
* If you are using a virtual network (vnet), ensure that the service endpoints are correctly configured for the Postgres server and the client. This can be done using the [Azure portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal) or the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli/).
* If you are using Private Link ensure the correct configuration of the [Private link](https://docs.microsoft.com/azure/postgresql/howto-configure-privatelink-portal)
* If you are using a Basic tier server, note that VNet service endpoints and [Private Link](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-private-link) are not supported
* If you are trying to connect to your server from an Azure PaaS service that doesn't have a static IP and doesn't support virtual networks, you can turn on [Allow access to Azure services](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules#connecting-from-azure). Turning this on opens the firewall to all Azure IPs.
* If the server's IP appears to be public and you can ping or connect using telnet, connections to the Azure Database for PostgreSQL server are routed through a publicly accessible Azure gateway. However, the actual server IP is protected by the firewall. For more information, visit the [connectivity architecture article](https://docs.microsoft.com/azure/postgresql/concepts-connectivity-architecture).

## **Recommended Documents**

* [Firewall rule concepts in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules)<br>
* [Use Virtual Network service endpoints and rules for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet/)<br>
* [Configure a VNET connection using Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli/)<br>
* [Configure a VNET connection using Portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal/)<br>
* [Configure a Private link using Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-privatelink-cli/)<br>
* [Configure a Private link using Portal](https://docs.microsoft.com/azure/postgresql/howto-configure-privatelink-portal/)<br>
* [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)<br>
* [Point to site connectivity using VNet service endpoints](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/securing-connectivity-to-azure-database-for-postgresql/ba-p/789591)<br>
* [Point to site connectivity using Private Link](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/using-private-link-and-point-to-site-gateway-for-secure-on/ba-p/1108165)<br>
* [Tutorial: Creating and connecting to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
