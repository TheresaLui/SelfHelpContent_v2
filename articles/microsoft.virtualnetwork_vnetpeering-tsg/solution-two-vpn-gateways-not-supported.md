<properties
pageTitle="Use Remote Gateway not supported when local vnet has gateway"
description="Use Remote Gateway not supported when local vnet has gateway"
infoBubbleText="Use Remote Gateway not supported when local vnet has gateway"
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="UseRemoteGatewaynotsupportedwhenlocalvnethasgateway"
diagnosticScenario="UseRemoteGatewaynotsupportedwhenlocalvnethasgateway"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>
# 'Use Remote Gateway' not supported when local vnet has a gateway
<!--issueDescription-->

This issue is a vnet peering restriction not allowing Vnet resources to 'use remote gateway' when the vnet they are in already has a vnet gateway. There is a reference to this restriction in the 'Use remote gateways' bullet in the ['Create a peering'](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#create-a-peering) section of this article. 

<!--/issueDescription-->


## **Recommended Steps**

1. Use the VNet gateway in the spoke VNet for outbound traffic ***or*** 
2. Remove the VNet gateway in the spoke VNet so you can use the remote 'hub' VNet's gateway.

## **Recommended Documents**

* [Peering Constraints](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering#create-a-peering)
