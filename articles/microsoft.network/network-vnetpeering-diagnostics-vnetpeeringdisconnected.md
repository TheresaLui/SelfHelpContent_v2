<properties
pageTitle="VNetPeeringDisconnected"
description="VNetPeeringDisconnected"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
ms.author="anavin"
displayOrder=""
articleId="VnetPeeringDisconnected"
diagnosticScenario="VNetPeeringMisConfigInsight"
selfHelpType="Diagnostics"
supportTopicIds="32584249"
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
ownershipId="CloudNet_VirtualNetwork"
/>

# We ran connectivity diagnostics on your resource and found an issue

<!--issueDescription-->
We have identified the virtual network peering "<!--$VirtualNetworkPeering-->VirtualNetworkPeering<!--/$VirtualNetworkPeering-->" is in **Disconnected** state because a previously created Virtual Network Peering link was deleted.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, delete this Virtual Network Peering link and then [recreate the connection](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering):

1. Sign in to the [Azure portal](http://portal.azure.com)
2. Select All Services > Virtual networks
3. Select the Virtual Network associated with the virtual network Peering
4. Click **Peerings** and select the virtual network Peering
5. Delete the virtual network peering
6. Recreate the connection
