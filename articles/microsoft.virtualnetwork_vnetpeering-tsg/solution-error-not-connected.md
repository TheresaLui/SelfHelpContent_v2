<properties
pageTitle="Solution For Not Connected Error"
description="Solution For Not Connected Error"
infoBubbleText="Solution For Not Connected Error"
service="microsoft.network"
ownershipId="Centennial_Cloudnet_VirtualNetwork"
resource="virtualnetwork"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="SolutionForNotConnectedError"
diagnosticScenario="SolutionForNotConnectedError"
selfHelpType="TSG_Content"
supportTopicIds=""
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
/>

# Solution For Not Connected Error
<!--issueDescription-->

This issue is typically caused when one side of the Vnet Peering is not configured for peering or has failed to complete peering.

<!--/issueDescription-->


## **Recommended Steps**

1. Delete peerings from all VNets involved
2. Recreate the peering between the VNets involved

## **Recommended Documents**

* [Troubleshoot a virtual network peering configuration error message](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-peering-issues#troubleshoot-a-virtual-network-peering-configuration-error-message)
