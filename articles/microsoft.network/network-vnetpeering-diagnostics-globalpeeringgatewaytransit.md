<properties
pageTitle="VNetPeeringGatewayTransit"
description="VNetPeeringGatewayTransit"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
ms.author="anavin"
displayOrder=""
articleId="GatewayWithVnetsInDifferentRegion"
diagnosticScenario="VNetPeeringGatewayTransit"
selfHelpType="Diagnostics"
supportTopicIds="32584249"
resourceTags="windows"
productPesIds="15526"
cloudEnvironments="Public"
/>
# We ran connectivity diagnostics on your resource and found an issue.
<!--issueDescription-->
Microsoft Azure has identified virtual network peering <!--$VirtualNetworkPeering-->VirtualNetworkPeering<!--/$VirtualNetworkPeering--> has the 'Use Remote Gateway' property enabled. Since this a globally peered link, this is not currently supported. Use VNet-to-VNet va VPN Gateway in  order to connect these virtual networks. [Learn how to properly configure Gateway Transit for VNet peering](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-peering-gateway-transit)
<br>