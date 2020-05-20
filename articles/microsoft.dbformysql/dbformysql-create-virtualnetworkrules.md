<properties
    pageTitle="Managing VNet service endpoints in Azure Database for MySQL"  
    description="Managing VNet service endpoints in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="220"
    selfHelpType="generic"
    supportTopicIds="32640097"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="62501419-052f-4574-bfca-0e75ed50141f"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Managing VNet service endpoints in Azure Database for MySQL

Virtual network rules are firewall rules that control whether your Azure Database for MySQL server accepts connections from a particular subnet in a virtual network. Virtual network rules can be configured using the Azure portal and Azure CLI.

## **Recommended Steps**

* Ensure that the Azure Database for MySQL uses the General Purpose or Memory optimized tier. The Basic tier does not support VNet service endpoints.
* If you are using multiple subscriptions make sure that both the subscription has the Microsoft.Sql resource provider registered. For more information refer [resource-manager-registration](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-supported-services) how-to
* If you are using multiple subscriptions all of them must be in the same Azure Active Directory tenant.
* Ensure that you have turned on [VNet service endpoints](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoints-overview) for your VNet
* To familiarize yourself with using ARM templates to create virtual network rules in Azure Database for MySQL server, refer to [Deploy multiple properties of a server including Firewall rules, Virtual Network rules, server parameters or databases](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithMultipleServerProperties) ARM template.
* If you are using the portal, review the [Configure a VNet connection using Portal](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal/) how-to
* If you are using the Azure CLI, review the [Configure a VNet connection using Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-cli/) how-to

## **Recommended Documents**

* [Use Virtual Network service endpoints and rules for Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-data-access-and-security-vnet/)
