<properties
pageTitle="Route Target null"
description="Route Target null"
infoBubbleText="Route Target null"
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
displayOrder=""
articleId="CantRDP_RouteTargetNull"
diagnosticScenario="Route Target Null"
selfHelpType="Diagnostic"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Connectivity Diagnostics Result

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. We identified that this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic has no route. If the routing result is not desired, view the Effective Route Table to determine cause, which may include User Defined Route (UDR) configuration, VPN tunnel learned routes, VNet Service Tunneling, or VNet Peering. To view effective routes:
1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account.
2. Click Browse > Network Interface.
3. Select the Network Interface of your VM
4. Click on the *Effective routes* blade
5. Modify the appropriate rule which is likely due to setting the destination IP address as an address in the Virtual Network.
 <br>
<!--/issueDescription-->
