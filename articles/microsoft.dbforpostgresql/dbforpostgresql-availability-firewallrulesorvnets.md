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
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="88983e2b-0ed3-4183-8eb3-24ecc5539e4e"
/>

# Managing firewall rules and virtual networks

[Firewall rules]((https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules)) or [virtual network service endpoints](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet) need to be configured to enable access to your Azure Database for PostgreSQL server.

## **Recommended Steps**

* You can either specify a single IP address or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the [Azure portal](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-portal), the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-firewall-using-cli), and our [REST API](https://docs.microsoft.com/rest/api/postgresql/).
* If you are using a virtual network (vnet), ensure that the service endpoints are correctly configured for the Postgres server and the client. This can be done using the [Azure portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal) or the [Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli/)
* If you are using a Basic tier server, note that VNet service endpoints are not supported.
* If you are trying to connect to your server from an Azure PaaS service that doesn't have a static IP and doesn't support virtual networks, you can turn on [Allow access to Azure services](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules#connecting-from-azure). Turning this on opens the firewall to all Azure IPs.

## **Recommended Documents**

* [Firewall rule concepts in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-firewall-rules)<br>
* [Use Virtual Network service endpoints and rules for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet/)<br>
* [Configure a VNET connection using Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli/)<br>
* [Configure a VNET connection using Portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal/)<br>
* [Troubleshoot common connectivity issues to Azure Databases for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-troubleshoot-common-connection-issues)<br>
* [Tutorial: Creating and connecting to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/tutorial-design-database-using-azure-portal/)
