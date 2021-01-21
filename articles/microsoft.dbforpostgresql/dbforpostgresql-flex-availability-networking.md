<properties
    pageTitle="Managing networking for Azure Database for PostgreSQL"
    description="Managing networing for Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="50"
    selfHelpType="generic"
    supportTopicIds="32780967"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-availability-networking"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Managing networking

Firewall rules or virtual networking must be configured to enable access to your Azure Database for PostgreSQL server.

## **Recommended Steps**

* You can either specify a single IP address or a range of IP addresses that are allowed to access your server. Server-level firewall rules can be managed through the Azure portal, the Azure CLI, and our REST API.
* If you are using a virtual network (VNet), ensure that the service endpoints are correctly configured for the Postgres server and the client. This can be done using the Azure portal or the Azure CLI.
* If you are trying to connect to your server from an Azure PaaS service that doesn't have a static IP and doesn't support virtual networks, you can turn on *Allow access to Azure IP addresses*. Turning this on opens the firewall to all IP addresses in Azure.
