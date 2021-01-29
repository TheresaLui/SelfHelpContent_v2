<properties
    pageTitle="Troubleshooting VNet connectivity issues"  
    description="Troubleshooting VNet connectivity issues"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="ankam"
    ms.author="ankam"
    displayOrder="240"
    selfHelpType="generic"
    supportTopicIds="32640028, 32780998"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dd2fe58d-ee46-42c8-a58a-b9775d8f84fb"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Managing VNet service endpoints in Azure Database for PostgreSQL

Virtual network rules are firewall rules that control whether your Azure Database for PostgreSQL server accepts connections from a particular subnet in a virtual network. Virtual network rules can be configured using the Azure portal and Azure CLI.

## **Recommended Steps**

* Ensure that the Azure Database for PostgreSQL uses the General Purpose or Memory Optimized tier. The Basic tier does not support VNet service endpoints.
* If you are using multiple subscriptions make sure that both the subscription has the Microsoft.Sql resource provider registered. For more information refer [resource-manager-registration](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-supported-services) how-to.
* If you are using multiple subscriptions all of them must be in the same Azure Active Directory tenant
* Ensure that you have turned on [VNet service endpoints](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoints-overview) for your VNet
* If you receive an error while trying to create a firewall rule, your server may have been unavailable due to a user- or service-initiated restart. You can review the Azure Activity Log for user-initiated operations like restart or scaling. You can review Resource Health Check for service availability.
* To familiarize yourself with using ARM templates to create virtual network rules in Azure Database for PostgreSQL server, refer to [Deploy multiple properties of a server including Firewall rules, Virtual Network rules, server parameters or databases](https://github.com/Azure/azure-postgresql/tree/master/arm-templates/ExampleWithMultipleServerProperties) ARM template.
* If you are using the portal, review the [Configure a VNet connection using Portal](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-portal/) how-to
* If you are using the Azure CLI, review the [Configure a VNet connection using Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-manage-vnet-using-cli/) how-to

## **Recommended Documents**

* [Use Virtual Network service endpoints and rules for Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/concepts-data-access-and-security-vnet/)
