<properties
    pageTitle="Managing Private link in Azure Database for PostgreSQL"  
    description="Managing Private link in Azure Database for PostgreSQL"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="220"
    selfHelpType="generic"
    supportTopicIds="32640947"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="a158b27f-fb25-4ef9-868b-b892c47cbce8"
/>

# Managing Private link in Azure Database for PostgreSQL

Private Link allows you to connect to various PaaS services in Azure via a private endpoint. Azure Private Link essentially brings Azure services inside your private Virtual Network (VNet). The PaaS resources can be accessed using the private IP address just like any other resource in the VNet.

## **Recommended Steps**

* Ensure that the Azure Database for PostgreSQL uses the General Purpose or Memory optimized tier. The Basic tier does not support Private link.
* If you are using the portal, review the [Configure a Private link using Portal](https://docs.microsoft.com/azure/postgresql/howto-configure-privatelink-portal) how-to
* If you are using the Azure CLI, review the [Configure a Private link using Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-privatelink-cli) how-to

## **Recommended Documents**

* [Use Private Link for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-private-link)
