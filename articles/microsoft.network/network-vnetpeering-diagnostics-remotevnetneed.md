<properties
pageTitle="RemoteVnetNeedEnableUseRemoteGateway"
description="RemoteVnetNeedEnableUseRemoteGateway"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
ms.author="anavin"
displayOrder=""
articleId="RemoteVnetNeedEnableUseRemoteGateway"
diagnosticScenario="RemoteVnetNeedEnableUseRemoteGateway"
selfHelpType="Diagnostics"
supportTopicIds="32584249"
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>

# We ran connectivity diagnostics on your resource and found an issue

<!--issueDescription-->
Microsoft Azure has identified virtual network peering  <!--$VirtualNetworkPeering-->[VirtualNetworkPeering]<!--/$VirtualNetworkPeering--> does not have "Use Remote Gateway" enabled, but <!--$VirtualNetworkPeering-->VirtualNetworkPeering<!--/$VirtualNetworkPeering--> has "Allow Gateway Transit" enabled.
<!--/issueDescription-->

## **Recommended Steps**

[Both of these settings need to be enabled](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-peering-gateway-transit) in order to successfully use the gateway for transit in VNet Peering.

Complete VNet Peering Connection:

1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account
2. Click All Services > Virtual networks
3. Select the Virtual Network associated with the VNet Peering
4. Click on the *Peerings* and select the VNet Peering
5. Check the box next to Allow Gateway Transit and click on Save
 
