<properties
    pageTitle="Managing VNet services endpoints for your Azure Database for MariaDB servers"
    description="Managing VNet services endpoints for your Azure Database for MariaDB servers"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="350"
    selfHelpType="generic"
    supportTopicIds="32640160"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="9a1c4ed4-2e58-4950-b361-44fda327f26f"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Managing VNet services endpoints for your Azure Database for MariaDB servers

Virtual Network (VNet) services endpoints and rules extend the private address space of a Virtual Network to your Azure Database for MariaDB server.

## **Recommended Steps**

* Ensure that your Azure Database for MariaDB is deployed in General Purpose and Memory Optimized servers. The Basic tier does not support VNet service endpoints.
* If the Azure resources being connected via service endpoints are across two subscriptions, make sure that the two subscriptions are in same Active directory tenant and both of them have **Microsoft.SQL** resource provider registered

## **Recommended Documents**

* [How-to create user in Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/howto-create-users)<br>
* [Azure Database for MariaDB Virtual network service endpoints](https://docs.microsoft.com/azure/mariadb/concepts-data-access-security-vnet/)<br>
* [Setting Virtual network service endpoints - Portal](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-portal/)<br>
* [Setting Virtual network service endpoints - CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-cli/)
