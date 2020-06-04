<properties
pageTitle="Solution for Global Virtual Network Peering Constraints"
description="Solution for Global Virtual Network Peering Constraints"
infoBubbleText="Solution for Global Virtual Network Peering Constraints"
service="microsoft.network"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionForGlobalVirtualNetworkPeeringConstraints"
diagnosticScenario="SolutionForGlobalVirtualNetworkPeeringConstraints"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
/>
# Solution for Global Virtual Network Peering Constraints
<!--issueDescription-->

This issue is a known constraint of peering virtual networks across regions otherwise known as 'global vnet peering'.

<!--/issueDescription-->

## **Recommended Steps**

1. Use a 'Standard' load balancer instead of a 'basic' load balancer or 
2. Connect your virtual networks by [creating a VNet-to-VNet gateway connection](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-vnet-vnet-resource-manager-portal)


## **Recommended Documents**

* https://docs.microsoft.com/azure/virtual-network/virtual-network-peering-overview#requirements-and-constraints
* https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-howto-vnet-vnet-resource-manager-portal
