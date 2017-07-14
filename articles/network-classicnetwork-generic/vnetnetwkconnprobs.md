<properties
	pageTitle="connectivity/othernetworkconnectivityproblems"
	description="connectivity/othernetworkconnectivityproblems"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32547255"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# connectivity/othernetworkconnectivityproblems

## **Recommended steps**
1. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade) to check if traffic is allowed to or from a virtual machine<br>
2. Use [Next hop](data-blade:microsoft_azure_network.getnexthopblade) for routes to find next hop type and IP address of packet from a specific VM and NIC<br>

## **Recommended documents**
[Network watcher overview](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitoring-overview)<br>
[Understanding outbound connections in Azure](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)<br>
[The secondary NIC is unable to connect to the network](https://docs.microsoft.com/azure/virtual-network/virtual-networks-multiple-nics#secondary-nics-access-to-other-subnets)<br>
