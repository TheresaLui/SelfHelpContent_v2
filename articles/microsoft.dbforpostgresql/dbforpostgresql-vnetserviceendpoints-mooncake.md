<properties
	pageTitle="Troubleshooting VNet connectivity issues"
	description="Troubleshooting VNet connectivity issues"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="ankam"
    ms.author="ankam,janeng"
	displayOrder="24"
	selfHelpType="resource"
	supportTopicIds="32640028"
	productPesIds="16222"
	cloudEnvironments="MoonCake"
	articleId="6f9ede8e-4659-4604-a28f-8cd6ab260a2b"
/>

# Troubleshooting VNet connectivity issues

VNet service endpoints are not supported in the Basic service tier of Azure Database for PostgreSQL.

## **Recommended Steps**

* Ensure the Microsoft.SQL service endpoint is enabled for your VNet
* Ensure your Azure Database for PostgreSQL has the correct firewall rules configure for your VNet

## **Recommended Documents**

* [Use Virtual Network service endpoints and rules for Azure Database for PostgreSQL](https://docs.azure.cn/postgresql/concepts-data-access-and-security-vnet/)
* [Configure a VNET-to-VNET connection using Azure CLI](https://docs.azure.cn/postgresql/howto-manage-vnet-using-cli/)
* [Configure a VNET-to-VNET connection using Portal](https://docs.azure.cn/postgresql/howto-manage-vnet-using-portal/)
