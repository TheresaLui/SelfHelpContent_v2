<properties
	pageTitle="connectivity/cannotconnecttoandfrominternet"
	description="connectivity/cannotconnecttoandfrominternet"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584250"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# connectivity/cannotconnecttoandfrominternet

## **Recommended steps**
1. Click [here](data-blade:microsoft_azure_network.NetworkWatcherConnectivityBlade.id.$subscriptionId) to troubleshoot connectivity issues to the internet<br>
2. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade) to check if traffic is allowed of denied to or from a VM<br>
3. Use [Next hop](data-blade:microsoft_azure_network.getnexthopblade) for routes to find next hop type and IP address of packet from a specific VM and NIC<br>
4. Use [Packet capture](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade) to track traffic to and from a VM<br>

## **Recommended documents**
[Troubleshoot Connectivity problems: Cannot connect to Internet](https://support.microsoft.com/help/4048050/troubleshooter-for-azure-vm-connectivity-problems)<br>
[Fix your Network Virtual Appliance (NVA)](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-nva)<br>
[Network watcher overview](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitoring-overview)<br>
[Understanding outbound connections in Azure](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)<br>
[Routing/Connecting to secondary NICs - Windows](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#routing-within-a-virtual-machine-operating-system-with-multiple-network-interfaces)<br>
[Routing/Connecting to secondary NICs - Linux](https://docs.microsoft.com/azure/virtual-machines/linux/multiple-nics#configure-guest-os-for-multiple-nics)
