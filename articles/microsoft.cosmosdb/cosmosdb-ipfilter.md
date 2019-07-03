<properties
	pageTitle="IP filter"
  	description="IP filter"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="bharathsreenivas"
	ms.author="bharathb"
	selfHelpType="generic"
	supportTopicIds="32636792"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-ipfilter"
/>

# Connecting to Azure Cosmos DB accounts

## **Recommended Steps**

### If you can't access your Cosmos DB account from the Azure Portal

* If you can't access your Cosmos DB account from the Azure Portal after enabling IP firewall or adding your account to a virtual network, make sure to tick the "Allow access from Azure Portal" checkbox on the "Firewall and virtual networks" section

### If you are having connectivity issues with your Cosmos DB account with IP firewall enabled

* You may have not added your IP address or IP address ranges in your account's firewall and virtual networks settings. To configure IP policy-based access control, you must provide the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account. Note that changes in firewall rules can take up to 15 minutes to apply.
* If you want to extend access to any Azure service, tick the "Accept connections from within public Azure datacenters" checkbox on the "Firewall and virtual networks" section

### If you are having connectivity issues while accessing Cosmos DB through a virtual network (VNet)

When using subnets, you have to:

* Enable [Service Endpoints](https://docs.microsoft.com/azure/cosmos-db/vnet-service-endpoint) on the subnet
* Make sure that the apps or services trying to connect to your Cosmos DB instance sit in the same virtual network and subnet as the Cosmos DB instance

If you want to extend access to any Azure service that's not part of the virtual network, tick the "Accept connections from within public Azure datacenters" checkbox on the "Firewall and virtual networks" section.

## **Recommended Documents**

* [IP firewall in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/firewall-support)
* [How to configure IP firewall in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-firewall)
* [Access Azure Cosmos DB from virtual networks (VNet)](https://docs.microsoft.com/azure/cosmos-db/vnet-service-endpoint)
* [How to configure access from virtual networks (VNet)](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-vnet-service-endpoint)
