<properties
pageTitle="Route Target Internet"
description="Route Target Internet"
infoBubbleText="Route Target Internet."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
displayOrder=""
articleId="CantRDP_RouteTargetInternet"
diagnosticScenario="Internet traffic"
selfHelpType="diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="public"
/>
# Connectivity Diagnostics Result

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->.
Routing <!--$action--> [action]<!--/$action--> this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic to route to the Internet.
Access Control {action} this {trafficDirection} traffic by default security rule: {rule.Replace("DefaultRule_", string.Empty)}.

If you do not wish traffic to this destination to be routed directly over the internet, either configure a route prefix covering this destination in your local VPN gateway, consult your network administrator to announce the prefix via BGP if you wish it to go over an ExpressRoute circuit or Site-to-Site VPN connection with BGP routing enabled, or add the prefix in a User Defined Route (UDR) if you wish to send the 
traffic to a Network Virtual Appliance (NVA).
If the access control (security rules) result is not desired, view the Effective Security Rules to determine if the addition or modification of a customer-defined security rule is required.

<!--/issueDescription-->