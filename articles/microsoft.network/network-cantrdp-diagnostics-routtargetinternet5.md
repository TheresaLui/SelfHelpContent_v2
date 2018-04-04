<properties
pageTitle="Route Target Internet"
description="Route Target Internet"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
displayOrder=""
articleId="CantRDP_RouteTargetInternet"
diagnosticScenario="Internet traffic"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public"
/>
# We ran connectivity diagnostics on your resource and found an issue.

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. We identified that this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic is <!--$StatelessAction-->[StatelessAction]<!--/$StatelessAction--> to route to the internet. 
<!--/issueDescription-->
If you do not want this traffic to this destination be routes directly over the internet:
1.  Configure a route prefix covering this destination in your local VPN gateway, consult your network administrator to announce the prefix via BGP if you want it to go over and ExpressRoute circuit or Site-toSite VPN connection with BGP routing enabled, 
2. or add the prefix in a User Defined Route (UDR) if you want to send the traffic to a Network Virtual Appliance (NVA)
 <br>

