<properties
	pageTitle="Diagnose and troubleshoot Azure connectivity issues to and from the internet"
	description="Diagnose and troubleshoot Azure connectivity issues to and from the internet"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	ms.author="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584250"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="1e7ff5db-a7c2-4165-93e7-1ec44b4f9583"
	ownershipId="CloudNet_VirtualNetwork"
/>

# Diagnose and troubleshoot Azure connectivity issues to and from the internet

## **Recommended Steps**

1. [Click to troubleshoot connectivity issues to the internet](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.sourceId.$resourceId)
2. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to check if traffic is allowed or denied to or from a VM<br>
3. Use [Next hop](data-blade:microsoft_azure_network.getnexthopblade.id.$subscriptionId) for routes to find next hop type and IP address of packet from a specific VM and NIC<br>
4. Use [Packet capture](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade.id.$subscriptionId) to track traffic to and from a VM<br>

## **Recommended Documents**

* [Troubleshoot Connectivity problems: Cannot connect to Internet](https://docs.microsoft.com/azure/virtual-network/troubleshoot-vm-connectivity)<br>
* [Fix your **Network Virtual Appliance (NVA)**](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva)<br>
* [Solve **VNet Peering** issues - Answer 3 questions](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-peering-issues)

<!--- THE ARTICLES BELOW HAVE A HISTORY OF NO CLICK THROUGH RATE (1/25/19)
[Network watcher overview](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitoring-overview)<br>
[Understanding outbound connections in Azure](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)<br>
[Routing/Connecting to secondary NICs - Windows](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#routing-within-a-virtual-machine-operating-system-with-multiple-network-interfaces)<br>
[Routing/Connecting to secondary NICs - Linux](https://docs.microsoft.com/azure/virtual-machines/linux/multiple-nics#configure-guest-os-for-multiple-nics)
-->
