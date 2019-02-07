<properties
	pageTitle="connectivity/VNET service endpoints"
	description="connectivity/VNET service endpoints"
	service="microsoft.dbformysql"
	resource="servers"
	authors="ankam"
    ms.author="ankam,janeng"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="32628413"
	productPesIds="16221"
	cloudEnvironments="public"
	articleId="d46364d3-7f26-4004-a67b-30c47cd73662"
/>

# Troubleshooting VNet connectivity issues

VNet service endpoints are not support in the Basic service tier of Azure Database for MySQL. For all other service tiers, work through the following checklist:

## **Recommended steps**

* Ensure the Microsoft.SQL service endpoint is enabled for your VNet
* Ensure your Azure Database for MySQL has the correct firewall rules configure for your VNet

## **Recommended documents**

[Use Virtual Network service endpoints and rules for Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-data-access-and-security-vnet/)<br>

[Configure a VNET-to-VNET connection using Azure CLI](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-cli/)<br>

[Configure a VNET-to-VNET connection using Portal](https://docs.microsoft.com/azure/mysql/howto-manage-vnet-using-portal/)
