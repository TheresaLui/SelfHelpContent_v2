<properties
pageTitle="Route Target VPN"
description="Route Target VPN"
infoBubbleText="Route Target VPN"
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
displayOrder=""
articleId="CantRDP_RouteTargetVPN"
diagnosticScenario="Inernet traffic"
selfHelpType="diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="public"
/>
# Connectivity Diagnostics Result

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. We identified that this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic is <!--$StatelessAction-->[StatelessAction]<!--/$StatelessAction--> to route via the Virual Network Gateway. If you do not want this traffic to pass over the Site-to-Site VPN connection either remove the prefix covering this destination from the [local network gateway configuration](https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-create-site-to-site-rm-powershell#modify) or remove it from the on premises BGP configuration in the event the VPN connection has BGP configured.
 <br>
<!--/issueDescription-->