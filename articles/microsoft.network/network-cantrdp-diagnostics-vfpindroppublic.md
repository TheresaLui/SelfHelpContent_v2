<properties
pageTitle="VfpInDropPublic"
description="VfpInDropPublic"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="CantRDP_VfpInDropPublic"
diagnosticScenario="MAC REWRITE"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>

# We ran connectivity diagnostics on your resource and found an issue

<!--issueDescription-->
Routing ALLOWS this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic when the source is NOT the Internet for CIDR prefixes advertised across a VPN tunnel, across an ExpressRoute Private peering, or CIDR prefixes used locally in the VNet or peered VNet.
<!--/issueDescription-->

## **Recommended Steps**

If the routing result is not desired, view the Effective Route Table to determine which tunnel is advertising a CIDR prefix covering this source IP address. Tunnels may include: VPN tunnels, ExpressRoute Private peering, VNet Peering, VNet Service Endpoints, or Forced Tunneling (Default Route) configuration.

1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account
2. Click Browse > Network Interface
3. Select the Network Interface of your VM
4. Click on the *Effective routes* blade
