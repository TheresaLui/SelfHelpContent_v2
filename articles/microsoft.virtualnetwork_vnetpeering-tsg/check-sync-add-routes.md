<properties
	pageTitle="TSG Content Step: Check VNet Integration Sync Status and Add Routes"
	description="TSG Content Step: Check VNet Integration Sync Status and Add Routes"
	service="microsoft.network"
	ownershipid="Centennial_Cloudnet_VirtualNetwork"
	resource="virtualnetwork"
	authors="chadmath"
	ms.author="chadmat"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="df84e7df-3b92-4a80-a404-87456b1eebb3"
/>

# Check VNet Integration Sync Status and Add Routes


## **Recommended Steps**

1. Have customer look in Vnet Integration section of the web app to verify you can see the remote Vnet
2. Manually enter in the remote Vnet address space ('Sync Network' & 'Add Routes') if it isn't found in above step
3. Workaround if customer does not want to use 'Preview' feature of VNet integration is to create Site-to-Site between the Vnets

## **Recommended Documents**

* [Sync Network Operation](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-sync-network-configuration)
* [Websites integrated with vnet](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet)
* [VPN Device has a resource for the P2S Client IP Range](https://docs.microsoft.com/azure/app-service/web-sites-integrate-with-vnet#accessing-on-premises-resources)
