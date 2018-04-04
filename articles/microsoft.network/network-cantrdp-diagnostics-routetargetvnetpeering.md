<properties
pageTitle="Route Target VNet Peering"
description="Route Target VNet Peering"
infoBubbleText= "Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
displayOrder=""
articleId="CantRDP_RouteTargetVNetPeering"
diagnosticScenario="Route Target VNet Peering"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public"
/>
# We ran connectivity diagnostics on your resource and found an issue.

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. We identified that this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic is <!--$StatelessAction-->[StatelessAction]<!--/$StatelessAction--> to route to the peered Virtual Network: <!--$VNetIdFromRuleName-->[$VNetIdFromRuleName]<!--$VNetIdFromRuleName-->. 
<!--/issueDescription-->
If you do not want traffic to be sent to peered Virtual Network, you can remove the peering as described [here](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering). Please note that this will break communication between the two Virtual Networks involved.
 <br>

