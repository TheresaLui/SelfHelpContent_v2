<properties
    pageTitle="Troubleshooting VNet connectivity issues"
    description="Troubleshooting VNet connectivity issues"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ankam"
    ms.author="ankam"
    displayOrder="240"
    selfHelpType="resource"
    supportTopicIds="32640028"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="dd2fe58d-ee46-42c8-a58a-b9775d8f84fb"
/>

# Managing VNet service endpoints in Azure Database for PostgreSQL

Virtual network rules are firewall rules that control whether your Azure Database for PostgreSQL server accepts connections from a particular subnet in a virtual network. Virtual network rules can be configured using the Azure portal and Azure CLI.

## **Recommended Steps**

* Ensure that the Azure Database for PostgreSQL uses the General Purpose or Memory Optimized tier. The Basic tier does not support VNet service endpoints.
* Ensure that you have turned on [VNet service endpoints](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoints-overview) for your VNet
* If you are using the portal, review the [Configure a VNet connection using Portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal/) how-to
* If you are using the Azure CLI, review the [Configure a VNet connection using Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli/) how-to

## **Recommended Documents**

* [Use Virtual Network service endpoints and rules for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet/)
