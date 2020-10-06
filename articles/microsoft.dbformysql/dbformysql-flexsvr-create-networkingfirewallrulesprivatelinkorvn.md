<properties
    pageTitle="Networking in Azure Databases for MySQL - Flexible Server"
    description="Networking in Azure Databases for MySQL - Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="150"
    selfHelpType="generic"
    supportTopicIds="32747628"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="f9cb4c29-6c2e-4155-9943-05b00171e589"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Networking in Azure Databases for MySQL - Flexible Server

Azure Database for MySQL Flexible Server supports two types of mutually exclusive network connectivity methods to connect to your flexible server. The two options are:

* Public access (allowed IP addresses)
* Private access (VNet Integration)

Please refer to recommended steps for respective section for resolving common issues.

## **Recommended Steps**

### Private access (VNet Integration)

* In order to create a flexible server in Private access (VNet Integration) using Azure Portal, you first need:
  * A [Virtual Network](https://docs.microsoft.com/azure/virtual-network/quick-create-portal#create-a-virtual-network)
  * To [delegate a subnet](https://docs.microsoft.com/azure/virtual-network/manage-subnet-delegation#delegate-a-subnet-to-an-azure-service) to **Microsoft.DBforMySQL/flexibleServers**. This delegation means that only Azure Database for MySQL Flexible Servers can use that subnet. No other Azure resource types can be in the delegated subnet.
* Creating a flexible server in Private access (VNet Integration) using Azure CLI delegates the subnet to **Microsoft.DBforMySQL/flexibleServers**. This delegation means that only Azure Database for MySQL Flexible Servers can use that subnet. No other Azure resource types can be in the delegated subnet.
* You can deploy your flexible server into a virtual network and subnet during server creation. After the flexible server is deployed, you cannot move it into another virtual network, subnet or to *Public access (allowed IP addresses)*.
* The virtual network and subnet should be in the same region and subscription as your flexible server
* Private access (VNet Integration) can be managed through the [Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-portal) or [Azure CLI](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-cli)

### Public access (allowed IP addresses)

* Make sure you have the right [firewall settings](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-networking#firewall-rules) in place to allow the desired access to your server. You can either specify a single IP addresses or a range of IP addresses that are allowed to access your server.
* Public access (allowed IP addresses) can be managed through the [Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-portal) and the [Azure CLI](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-cli)

## **Recommended Documents**

* [Networking overview](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-networking)
* Learn how to enable private access (vnet integration) using the [Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-portal) or [Azure CLI](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-virtual-network-cli)
* Learn how to enable public access (allowed IP addresses) using the [Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-portal) or [Azure CLI](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-cli)
* Learn how to [connect using TLS/SSL](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-connect-tls-ssl)