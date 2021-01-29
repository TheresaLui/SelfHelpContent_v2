<properties
pageTitle="Bypassing UDR Solution"
description="Bypassing UDR Solution"
infoBubbleText="Bypassing UDR Solution"
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="VnetPeeringBypassingUdrSolution"
diagnosticScenario="VnetPeeringBypassingUdrSolution"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>
# User-Defined Route Blocking Traffic to Resource
<!--issueDescription-->

This issue was caused by user-defined route (UDR) **'<!--$UDR-->[UDRName]<!--/$UDR-->'** that was blocking traffic from reaching the destination. By default, VMs in the same virtual network and peered virtual network can communicate with one another due to a system routing rule allowing intra Virtual Network connectivity. More information is available in online docs Virtual network traffic routing referenced below. I realize any UDRs blocking intra Vnet connectivity are typically intentional and for security compliance reasons. I've included some diagnostic tools available to you to help identify this type of issue in the future.

<!--/issueDescription-->


## **Recommended Steps**

* Remove the UDR that was blocking or
* Create a routing rule with a higher (more specific) CIDR reference, such as, /32

## **Recommended Documents**

* [Diagnose VM Network Traffic Filter Problem](https://docs.microsoft.com/azure/network-watcher/diagnose-vm-network-traffic-filtering-problem)
* [Diagnose VM routing problems](https://docs.microsoft.com/azure/network-watcher/network-watcher-next-hop-overview)
