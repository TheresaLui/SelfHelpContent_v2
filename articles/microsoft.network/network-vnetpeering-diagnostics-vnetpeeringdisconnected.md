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
cloudEnvironments="Public, Fairfax"
	ownershipId="CloudNet_VirtualNetwork"
/>

# We ran connectivity diagnostics on your resource and found an issue

<!--issueDescription-->
Microsoft Azure has identified virtual network peering <!--$VirtualNetworkPeering-->VirtualNetworkPeering<!--/$VirtualNetworkPeering--> is in Disconnected state traffic because a previously created Virtual Network Peering link was deleted.
<!--/issueDescription-->

## **Recommended Steps**

In order to create the virtual network peering, delete this link and [recreate the connection](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering):

1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account
2. Click All Services > Virtual networks
3. Select the Virtual Network associated with the VNet Peering
4. Click on the *Peerings* and select the VNet Peering
5. Delete the VNet peering
