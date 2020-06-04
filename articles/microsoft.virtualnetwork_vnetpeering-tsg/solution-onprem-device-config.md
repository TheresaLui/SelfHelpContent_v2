<properties
pageTitle="Solution on prem device config remote IP update"
description="Solution on prem device config remote IP update"
infoBubbleText="Solution on prem device config remote IP update"
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionOnPremDeviceConfigRemoteIpUpdate"
diagnosticScenario="SolutionOnPremDeviceConfigRemoteIpUpdate"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>
# On-premises device configuration missing remote VNet IPs
<!--issueDescription-->

We identified the issue was caused by the on-premises device not having the peered VNets IPs configured as 'interesting traffic'. Because of this, it did not route traffic destined for the peered VNet IP ranges over the VPN tunnel. The routes need to be added manually or the VPN gateways and peers must be setup for BPG so the routes are learned automatically. More information is available in online docs Virtual network traffic routing referenced below.

<!--/issueDescription-->

## **Recommended Documents**

* [BGP with Azure VPN Gateway](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-bgp-overview)

