<properties
pageTitle="VNetPeeringInitiated"
description="VNetPeeringInitiated"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
ms.author="anavin"
displayOrder=""
articleId="PeeringInitiatedDifferentSub"
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
Microsoft Azure has identified virtual network peering <!--$VirtualNetworkPeering-->VirtualNetworkPeering<!--/$VirtualNetworkPeering--> is in an *Initiated* state. Virtual Network Peering requires two links to be created. In order to create the virtual network peering successfully, create the second link.
<!--/issueDescription-->

## **Recommended Steps**

1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account
2. Click All Services > Virtual networks
3. Select the Virtual Network associated with the VNet Peering
4. Click on the *Peerings* and select the VNet Peering
5. Select the peer Virtual Network and create a link from the peer Virtual Network to the one you selected
 <br>
