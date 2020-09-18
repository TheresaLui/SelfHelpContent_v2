<properties
pageTitle="Bypassing NSG Solution"
description="Bypassing NSG Solution"
infoBubbleText="Bypassing NSG Solution"
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="VnetPeeringBypassingNsgSolution"
diagnosticScenario="VnetPeeringBypassingNsgSolution"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>
# NSG Blocking Traffic to Resource
<!--issueDescription-->

This issue was caused by network security group (NSG) policy **'<!--$NSG-->[NsgName]<!--/$NSG-->'** that was blocking traffic from reaching the destination. By default, VMs in the same virtual network and peered virtual network can communicate with one another due to a system routing rule allowing intra Virtual Network connectivity. More information is available in online docs Virtual network traffic routing referenced below. I realize any NSGs blocking intra Vnet connectivity are typically intentional and for security compliance reasons. I've included some diagnostic tools available to you to help identify this type of issue in the future.

<!--/issueDescription-->


## **Recommended Steps**

* Remove the NSG that was blocking or
* Create an allow rule with a higher priority (lower number)

## **Recommended Documents**

* [Diagnose VM Network Traffic Filter Problem](https://docs.microsoft.com/azure/network-watcher/diagnose-vm-network-traffic-filtering-problem)
* [Diagnose VM routing problems](https://docs.microsoft.com/azure/network-watcher/network-watcher-next-hop-overview)
