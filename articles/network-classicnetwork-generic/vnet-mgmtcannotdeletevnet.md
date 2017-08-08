<properties
	pageTitle="management/cannotdeletevirtualnetwork"
	description="management/cannotdeletevirtualnetwork"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv,anavinahar"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584253"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# management/cannotdeletevirtualnetwork

## **Recommended steps**
1. Check connected devices to your virtual network from [Network watcher topology](data-blade:microsoft_azure_network.networkwatchertopologyblade)<br>
2. Ensure to remove all devices from the virtual network before deleting. The reccommended deletion order is gateway connections, gateways, IPs, VNet Peerings, App Service Environment. Detailed steps can be found on the [Troubleshoor cannot delete VNet article](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet#check-whether-a-virtual-network-gateway-is-running-in-the-virtual-network)<br>

## **Recommended documents**
[Troubleshoot cannot delete VNet](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet)
[Delete a virtual network gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-delete-vnet-gateway-portal)
