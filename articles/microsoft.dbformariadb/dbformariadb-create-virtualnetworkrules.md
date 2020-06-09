<properties
    pageTitle="Managing VNet service endpoints in Azure Database for MariaDB"
    description="Managing VNet service endpoints in Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam" 
    ms.author="andrela"
    displayOrder="220"
    selfHelpType="generic"
    supportTopicIds="32640159"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="954b5c88-d513-435a-b878-0cd6d50f8eba"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Managing VNet service endpoints in Azure Database for MariaDB

Virtual network rules are firewall rules that control whether your Azure Database for MariaDB server accepts connections from a particular subnet in a virtual network. Virtual network rules can be configured using the Azure portal and Azure CLI.

## **Recommended Steps**

* Ensure that the Azure Database for MariaDB uses the General Purpose or Memory optimized tier. The Basic tier does not support VNet service endpoints.
* If you are using multiple subscriptions make sure that both the subscription has the Microsoft.Sql resource provider registered. For more information refer to the [resource-manager-registration](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-supported-services) how-to.
* If you are using multiple subscriptions, all of them must be in the same Azure Active Directory tenant
* Ensure that you have turned on [VNet service endpoints](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoints-overview) for your VNet
* To familiarize yourself with using ARM templates to create virtual network rules in Azure Database for MariaDB server, refer to [Deploy multiple properties of a server including Firewall rules, Virtual Network rules, server parameters or databases](https://github.com/Azure/azure-mariadb/tree/master/arm-templates/ExampleWithMultipleServerProperties) ARM template
* If you are using the portal, review the [Configure a VNet connection using Portal](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-portal/) how-to
* If you are using the Azure CLI, review the [Configure a VNet connection using Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-cli/) how-to

## **Recommended Documents**

* [Use Virtual Network service endpoints and rules for Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-data-access-security-vnet/)
