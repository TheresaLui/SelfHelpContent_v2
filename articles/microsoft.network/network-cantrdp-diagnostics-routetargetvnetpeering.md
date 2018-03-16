<properties
pageTitle="Route Target VNet Peering"
description="Route Target VNet Peering"
infoBubbleText="Route Target VNet Peering."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
displayOrder=""
articleId="CantRDP_RouteTargetVNetPeering"
diagnosticScenario="Route Target VNet Peering"
selfHelpType="Diagnostic"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public"
/>
# Connectivity Diagnostics Result

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. We identified that this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic is <!--$StatelessAction-->[StatelessAction]<!--/$StatelessAction--> to route to the peered Virtual Network: <!--$VNetIdFromRuleName-->[$VNetIdFromRuleName]<!--$VNetIdFromRuleName-->. If you do not want traffic to be sent to peered Virtual Network, you can remove the peering as described [here](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-peering). Please note that this will break communication between the two Virtual Networks involved.
 <br>
<!--/issueDescription-->
