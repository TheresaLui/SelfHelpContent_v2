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
1. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade) to check if traffic is allowed of denied to or from a VM<br>
2. Use [Security group view](data-blade:microsoft_azure_network.networkwatchersecuritygroupviewblade) to see NSGs and rules associated at a NIC and subnet level for VM<br>
3. Use [Next hop](data-blade:microsoft_azure_network.getnexthopblade) for routes to find next hop type and IP address of packet from a specific VM and NIC<br>
4. Use [NSG flow logs](data-blade:microsoft_azure_network.flowlogsblade) to view ingress and egress IP traffic through a Network Security Group<br>
5. Use [Packet capture](data-blade:microsoft_azure_network.networkwatcherpacketcaptureblade) to track traffic to and from a VM<br>

## **Recommended documents**
[Network watcher overview](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitoring-overview)<br>
[Understanding outbound connections in Azure](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections)<br>
[Routing/Connecting to secondary NICs - Windows](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#routing-within-a-virtual-machine-operating-system-with-multiple-network-interfaces)<br>
[Routing/Connecting to secondary NICs - Linux](https://docs.microsoft.com/azure/virtual-machines/linux/multiple-nics#configure-guest-os-for-multiple-nics)