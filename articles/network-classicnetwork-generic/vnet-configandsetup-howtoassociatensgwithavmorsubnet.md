<properties
	pageTitle="configurationandsetup/howtoassociateansgwithavmorsubnet"
	description="configurationandsetup/howtoassociateansgwithavmorsubnet"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584255"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# configurationandsetup/howtoassociateansgwithavmorsubnet

## **Recommended steps**
1. Use [Security group view](data-blade:microsoft_azure_network.networkwatchersecuritygroupviewblade) to see NSGs and rules associated at a NIC and subnet level for VM<br>
2. Use [Next hop](data-blade:microsoft_azure_network.getnexthopblade) for routes to find next hop type and IP address of packet from a specific VM and NIC<br>

## **Recommended documents**
[Associating NSGs to VMs, NICs or subnets](https://docs.microsoft.com/azure/virtual-network/virtual-networks-nsg#associating-nsgs)<br>
[Create NSGs](https://docs.microsoft.com/azure/virtual-network/virtual-networks-create-nsg-arm-pportal)
[Create a DMZ in classic](https://docs.microsoft.com/azure/virtual-network/virtual-networks-dmz-nsg-asm)
[Create a DMZ between Azure and the internet in ARM](https://docs.microsoft.com/azure/architecture/reference-architectures/dmz/secure-vnet-dmz)
