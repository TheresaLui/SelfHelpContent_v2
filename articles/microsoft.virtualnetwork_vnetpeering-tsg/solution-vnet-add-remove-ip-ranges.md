<properties
	pageTitle="Error VNet address space overlap"
	description="Error VNet address space overlap"
	service="microsoft.network"
	resource="virtualNetwork"
	authors="chadmath"
	ms.author="chadmat"
	diagnosticScenario="ErrorVNetAddressSpaceOverlap"
	selfHelpType="TSG_Content"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	articleId="f9bdf545-36ab-4684-b7c8-22ad4478a130"
	ownershipId="Centennial_Cloudnet_VirtualNetwork"
	supportTopicIds=""
    resourceTags="windows"
    productPesIds="15526"
/>

# Solution for VNet address space overlap
<!--issueDescription-->

Through our investigation we found that you cannot add or delete IP ranges from a VNet that has an active peering. Please refer to the steps and articles below for more information on the limitations and options to peer these VNets.

<!--/issueDescription-->

## **Recommended Steps

1. Delete the peerings on both VNets
2. Add or remove the address ranges
3. Then re-create the peerings between the two VNets

## **Recommended Documents**

* [Vnet Peering Constraints](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#requirements-and-constraints)
* [Manage Virtual Networks](https://docs.microsoft.com/azure/virtual-network/manage-virtual-network)
