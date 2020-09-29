<properties
	pageTitle="connectivity/cannotconnecttoanothervirtualmachineinthesamevnet"
	description="connectivity/cannotconnecttoanothervirtualmachineinthesamevnet"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584252"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="118399a2-440f-44c4-80b7-1c364ec51f01"
	ownershipId="CloudNet_VirtualNetwork"
/>

# connectivity/cannotconnecttoanothervirtualmachineinthesamevnet

## **Recommended Steps**

1. [Troubleshoot connectivity issues](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.sourceId.$resourceId)
2. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to check if traffic is allowed to or from a virtual machine<br>
3. Use [Next hop](data-blade:microsoft_azure_network.getnexthopblade.id.$subscriptionId) for routes to find next hop type and IP address of packet from a specific VM and NIC<br>

## **Recommended Documents**

* [Troubleshoot your **Network Virtual Appliance (NVA)**](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva)<br>
* [Troubleshoot Connectivity problems: Cannot connect to another Azure VM in same Virtual Network](https://docs.microsoft.com/azure/virtual-network/troubleshoot-vm-connectivity)<br>
* [Solve **VNet Peering** issues - Answer 3 questions](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-peering-issues)<br>
* [Troubleshoot Network Security Groups](https://docs.microsoft.com/azure/virtual-network/virtual-network-nsg-troubleshoot-portal)<br>
* [Troubleshoot Routes](https://docs.microsoft.com/azure/virtual-network/virtual-network-routes-troubleshoot-portal)

