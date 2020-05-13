<properties
	pageTitle="I can't connect to my secondary NIC"
	description="Troubleshoot connectivity issues to your secondary network interface card (NIC)"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="anavin"
	ms.author="anavin"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="86c8a9e2-be63-48b7-90a2-ca6a37fd5e0c"
	ownershipId="CloudNet_VirtualNetwork"
/>

# I can't connect to my secondary NIC

## **Recommended Steps**

To resolve the most common issues, try one or more of the following methods.

1. Make sure you have successfully added multiple NICs to your VM:

	* [Create a VM (Classic/RDFE) with multiple NICs](https://docs.microsoft.com/azure/virtual-network/virtual-network-deploy-multinic-classic-ps)
	* [View network interfaces for a VM](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#vm-view-nic)
	
2. Azure does not assign a default gateway to additional (secondary) network interfaces attached to a virtual machine. Therefore, you are unable to communicate with resources outside the subnet that a secondary network interface is in, by default. Secondary network interfaces can, however, communicate with resources outside their subnet, though the steps outlined below to enable communication are different for different operating systems:

	* [Windows](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#routing-within-a-virtual-machine-operating-system-with-multiple-network-interfaces)
	* [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/multiple-nics#configure-guest-os-for-multiple-nics)<br>

## **Recommended Documents**

* [Routing/Connecting to secondary NICs - Windows](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#routing-within-a-virtual-machine-operating-system-with-multiple-network-interfaces)<br>
* [Routing/Connecting to secondary NICs - Linux](https://docs.microsoft.com/azure/virtual-machines/linux/multiple-nics#configure-guest-os-for-multiple-nics)
