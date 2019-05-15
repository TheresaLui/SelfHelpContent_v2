<properties
	pageTitle="connectivity/VNET service endpoints"
	description="connectivity/VNET service endpoints"
	service="microsoft.dbformariadb"
	resource="servers"
	authors="ajlam"
    ms.author="andrela"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="32640123"
	productPesIds="16617"
	cloudEnvironments="public"
	articleId="mariadbvnetconnect"
/>

# Troubleshooting VNet connectivity issues

VNet service endpoints are not supported in the Basic service tier of Azure Database for MariaDB.

## **Recommended Steps**

* Ensure the Microsoft.SQL service endpoint is enabled for your VNet
* Ensure your Azure Database for MariaDB has the correct firewall rules configure for your VNet

## **Recommended Documents**

* [Use Virtual Network service endpoints and rules for Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-data-access-security-vnet/)<br>
* [Configure a VNET-to-VNET connection using Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-cli/)<br>
* [Configure a VNET-to-VNET connection using Portal](https://docs.microsoft.com/azure/mariadb/howto-manage-vnet-portal/)
