<properties
pageTitle="SolutionGatewayTransitConfiguration"
description="SolutionGatewayTransitConfiguration"
infoBubbleText="SolutionGatewayTransitConfiguration"
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionGatewayTransitConfiguration"
diagnosticScenario="SolutionGatewayTransitConfiguration"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>
# VNet Peering Gateway Transit Misconfiguration
<!--issueDescription-->

This issue was due to gateway transit configuration for VNet Peering. We found the spoke VNet without the gateway needs to be set to 'Use Remote Gateway' in the Peering settings and the hub VNet with the gateway needs to be set to 'Allow gateway transit'.

<!--/issueDescription-->


## **Recommended Documents**

* [Configure VPN Gateway transit for virtual network peering](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-peering-gateway-transit?toc=%2fazure%2fvirtual-network%2ftoc.json)
