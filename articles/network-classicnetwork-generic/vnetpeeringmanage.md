<properties
	pageTitle="vnetpeering/managevnetpeering"
	description="vnetpeering/managevnetpeering"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32547254"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# vnetpeering/managevnetpeering

## **Recommended documents**
[VNet Peering](https://docs.microsoft.com/azure/virtual-network/virtual-network-peering-overview)

## **Frequently asked questions**
### **I created a peering, why am I not able to ping the VM in the peer VNet?**
Make sure the peering status says *Connected*. If the peering status is *Initiated*, only one link has been created. So successfully peer, you will need to establish two peering links. Read the [Create a virtual netwrok peering](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-create-vnetpeering-arm-portal) article to see a step by step tutorial on how this can be done.

### **Is transitive VNet peering possible?**
VNet peering is between two VNets, there is no derived transitive relationship across peerings. For example, if VNet A is peered with VNet B, and VNet B is peered with VNet C, VNetA is not peered to VNetC. In order to establish a connection between VNet A and C, they must be peered.

### **How do I peer across subscriptions?**
In order to peer across subscriptions, you need certain permissions over subscriptions. The [Peering across subscriptions](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-create-vnetpeering-arm-portal#a-namex-subapeering-across-subscriptions) article shows you how this can be done.
