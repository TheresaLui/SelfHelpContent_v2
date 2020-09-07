<properties
pageTitle="Service Chaining Requirements Not Met Solution"
description="Service Chaining Requirements Not Met Solution"
infoBubbleText="Service Chaining Requirements Not Met Solution"
service="microsoft.network"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="ServiceChainingRequirementsNotMetSolution"
diagnosticScenario="ServiceChainingRequirementsNotMetSolution"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, fairfax, usnat, ussec"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Service Chaining Requirements Not Met
<!--issueDescription-->

This issue was caused by configuration of the service chaining requirements not being fully met. The requirements consist of a NVA in the hub VNet with UDRs in the spokes pointing to the NVA IP in the hub VNet. It also requires configuration of the NVA device which can vary depending on the vendor of the NVA. More information and resources are included below.

<!--/issueDescription-->


## **Recommended Steps**

* Remove the NSG that was blocking or
* Create an allow rule with a higher priority (lower number)

## **Recommended Documents**

* [Troubleshoot NVA issues in Azure](https://docs.microsoft.com/azure/network-watcher/diagnose-vm-network-traffic-filtering-problem)
* [Diagnose VM routing problems](https://docs.microsoft.com/azure/network-watcher/network-watcher-next-hop-overview)
* [Network Watcher Topology View](https://docs.microsoft.com/azure/network-watcher/view-network-topology)

