<properties
pageTitle="Route Target Internet"
description="Route Target Internet"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
ms.author="anavin"
displayOrder=""
articleId="CantRDP_RouteTargetInternet"
diagnosticScenario="Internet traffic"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>

# We ran connectivity diagnostics on your resource and found an issue

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. Routing <!--$action-->[action]<!--/$action--> this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic to route to the Internet.
<!--/issueDescription-->

## **Recommended Steps**

If you do not wish traffic to this destination to be routed directly over the internet, either configure a route prefix covering this destination in your local VPN gateway, consult your network administrator to announce the prefix via BGP if you wish it to go over an ExpressRoute circuit or Site-to-Site VPN connection with BGP routing enabled, or add the prefix in a User Defined Route (UDR) if you wish to send the traffic to a Network Virtual Appliance (NVA).

If the access control (security rules) result is not desired, view the [Effective Security Rules](https://docs.microsoft.com/azure/virtual-network/virtual-network-nsg-troubleshoot-portal) to determine the customer-defined security rule requiring modification. If this traffic should be allowed, create a <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> basic rule with a higher priority (lower number) than existing rules specifying port {this.destinationPort}. If this traffic should not be allowed, create a <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> advanced rule with a higher priority (lower number) than existing rules specifying the source and destination IPs desired, port {this.destinationPort}, and action Deny.
