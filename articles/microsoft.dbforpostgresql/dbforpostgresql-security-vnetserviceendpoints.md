<properties
    pageTitle="Managing VNet service endpoints for your Azure Database for PostgreSQL servers"
    description="Managing VNet service endpoints for your Azure Database for PostgreSQL servers"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="440"
    selfHelpType="resource"
    supportTopicIds="32640029"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="650bfaca-c013-49b7-a158-eba8cf126181"
/>

# Managing VNet service endpoints for your Azure Database for PostgreSQL servers

Virtual Network (VNet) service endpoints and rules extend the private address space of a Virtual Network to your Azure Database for PostgreSQL server.

## **Recommended Steps**

* Ensure that your Azure Database for PostgreSQL is deployed in General Purpose and Memory Optimized servers. The Basic tier does not support VNet service endpoints.
* If the Azure resources being connected via service endpoints are across two subscriptions, make sure that the two subscriptions are in same Active directory tenant and both of them have **Microsoft.SQL** resource provider registered

## **Recommended Documents**

* [How-to create user in Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-create-users)<br>
* [Azure Database for PostgreSQL Virtual network service endpoints](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet)<br>
* [Setting Virtual network service endpoints - Portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal)<br>
* [Setting Virtual network service endpoints - CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli)
