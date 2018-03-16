<properties
pageTitle="Traffic from Internet"
description="Traffic from Internet"
infoBubbleText="Traffic from Internet"
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
displayOrder=""
articleId="CantRDP_TrafficfromInternet"
diagnosticScenario="Traffic from Internet"
selfHelpType="Diagnostic"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Connectivity Diagnostics Result
<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. We identified that this  <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic is  <!--$StatelessAction-->[StatelessAction]<!--/$StatelessAction--> when the source is from the internet for CIDR prefixes advertised across a VPN tunnel, or CIDR prefixes used locally in the VNet or peered VNet. If the routing result is not desired, view the Effective routes to determine which tunnel is advertising a CIDR prefix covering this source IP address. Tunnels may include: VPN tunnels, VNet Peering, VNet Service Tunneling, or Forced Tunneling (Default Route) configuration. To view the Effective routes: 
1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account.
2. Click Browse > Network Interface.
3. Select the Network Interface of your VM
4. Click on the *Effective routes* blade
5. Modify the appropriate rule which is likely due to setting the destination IP address as an address in the Virtual Network.
 <br>
<!--/issueDescription-->
