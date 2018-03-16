<properties
pageTitle="VfpInDropPublic"
description="VfpInDropPublic"
infoBubbleText="VfpInDropPublic"
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
displayOrder=""
articleId="CantRDP_MAC REWRITE"
diagnosticScenario="MAC REWRITE"
selfHelpType="Diagnostic"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Connectivity Diagnostics Result

<!--issueDescription-->
Routing ALLOWS this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic when the source is NOT the Internet for CIDR prefixes advertised across a VPN tunnel, across an ExpressRoute Private peering, or CIDR prefixes used locally in the VNet or peered VNet. If the routing result is not desired, view the Effective Route Table to determine which tunnel is advertising a CIDR prefix covering this source IP address. Tunnels may include: VPN tunnels, ExpressRoute Private peering, VNet Peering, VNet Service Endpoints, or Forced Tunneling (Default Route) configuration. 

1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account.
2. Click Browse > Network Interface.
3. Select the Network Interface of your VM
4. Click on the *Effective routes* blade
<br>
<!--/issueDescription-->
