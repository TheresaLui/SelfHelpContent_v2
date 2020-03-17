<properties
    pageTitle="I can't connect to my secondary NIC"
    description="I can't connect to my secondary NIC"
    service="microsoft.network"
    resource="virtualnetworks"
    authors="anavin"
    ms.author="anavin"
    displayOrder="18"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="8115f445-c9e0-43c4-8e88-ed594d14fae8"
	ownershipId="CloudNet_VirtualNetwork"
/>

# I can't connect to my secondary NIC

## **Recommended Steps**

To resolve most common issues, try one or more of the following methods:

1. Make sure you have successfully added multiple Network Interface Controllers (NICs) to your VM:

    * [Create a VM (Classic/RDFE) with multiple NICs](https://docs.azure.cn/virtual-network/virtual-network-deploy-multinic-classic-ps)
    * [View network interfaces for a VM](https://docs.azure.cn/virtual-network/virtual-network-network-interface-vm#vm-view-nic)

2. Azure does not assign a default gateway to additional (secondary) network interfaces attached to a virtual machine. By default, you are unable to communicate with resources outside the subnet that a secondary network interface is in. Secondary network interfaces can, however, communicate with resources outside their subnet. To enable communication, follow the steps outlined below for the appropriate operating system: 

    * [Windows](https://docs.azure.cn/virtual-network/virtual-network-network-interface-vm#routing-within-a-virtual-machine-operating-system-with-multiple-network-interfaces)
    * [Linux](https://docs.azure.cn/virtual-machines/linux/multiple-nics#configure-guest-os-for-multiple-nics)<br>

## **Recommended Documents**

* [Routing/Connecting to secondary NICs - Windows](https://docs.azure.cn/virtual-network/virtual-network-network-interface-vm#routing-within-a-virtual-machine-operating-system-with-multiple-network-interfaces)<br>
* [Routing/Connecting to secondary NICs - Linux](https://docs.azure.cn/virtual-machines/linux/multiple-nics#configure-guest-os-for-multiple-nics)
