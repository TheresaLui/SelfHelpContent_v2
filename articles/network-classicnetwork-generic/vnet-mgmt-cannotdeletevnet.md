<properties
	pageTitle="management/cannotdeletevirtualnetwork"
	description="management/cannotdeletevirtualnetwork"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="anavinahar"
	ms.author="anavin"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584253"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="627dab53-d2ea-4306-9b46-a93a32bba7be"
	ownershipId="CloudNet_VirtualNetwork"
/>

# management/cannotdeletevirtualnetwork

## **Recommended Steps**

1. Check connected devices to your virtual network from [Network watcher topology](data-blade:microsoft_azure_network.networkwatchertopologyblade.id.$resourceId)<br>
2. Ensure to remove all connected devices from the virtual network before deleting. The recommended deletion order is gateway connections, gateways, IPs, VNet Peerings, App Service Environment. Detailed steps can be found on the [Troubleshoot cannot delete VNet article](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet#check-whether-a-virtual-network-gateway-is-running-in-the-virtual-network).

## **Recommended Documents**

* [Troubleshoot cannot delete VNet](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet)<br>
* [Delete a virtual network gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-delete-vnet-gateway-portal)
