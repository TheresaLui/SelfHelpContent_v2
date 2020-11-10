<properties
    pageTitle="Managing VNet services endpoints for your Azure Database for MySQL servers"
    description="Managing VNet services endpoints for your Azure Database for MySQL servers"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="390"
    selfHelpType="generic"
    supportTopicIds="32640098"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="168ab2c1-a474-4155-8cf6-77a03bb8ef9a"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Managing VNet services endpoints for your Azure Database for MySQL servers

Virtual Network (VNet) services endpoints and rules extend the private address space of a Virtual Network to your Azure Database for MySQL server.

## **Recommended Steps**

* Ensure that your Azure Database for MySQL is deployed in General Purpose and Memory Optimized servers. The Basic tier does not support VNet service endpoints.
* If the Azure resources being connected via service endpoints are across two subscriptions, make sure that the two subscriptions are in same Active directory tenant and both of them have **Microsoft.SQL** resource provider registered

### Private Link

* If you are using Private Link ensure the correct configuration of the [Private link](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal)
* If you are using a Basic tier server, note that [Private Link](https://docs.microsoft.com/azure/mysql/concepts-data-access-security-private-link) is not supported

## **Recommended Documents**

* [How-to create user in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-create-users)<br>
* [Azure Database for MySQL Virtual network service endpoints](https://docs.microsoft.com/azure/mysql/concepts-data-access-and-security-vnet)<br>
* [Setting Virtual network service endpoints - Portal](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal)<br>
* [Setting Virtual network service endpoints - CLI](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-cli)
