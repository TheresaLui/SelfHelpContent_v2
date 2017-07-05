<properties
	pageTitle="management/cannotdeletevirtualnetwork"
	description="management/cannotdeletevirtualnetwork"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
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
2. Ensure to remove all devices from the virtual network before deleting. Proper deletion order is connections, gateways, IPs and VNets<br>

## **Recommended documents**
[Delete a virtual network gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-delete-vnet-gateway-portal)