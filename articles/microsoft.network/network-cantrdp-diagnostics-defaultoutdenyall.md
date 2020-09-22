<properties
pageTitle="DefaultOutDenyAll"
description="DefaultOutDenyAll"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="CantRDP_DefaultOutDenyAll"
diagnosticScenario="DefaultOutDenyAll"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>
# We ran connectivity diagnostics on your resource and found an issue

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. We identified that this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic is <!--$StatefulAction-->[StatefulAction]<!--/$StatefulAction--> by a default security rule: <!--$RuleNameWithDefaultRule_RemovedFromBeginning-->[RuleNameWithDefaultRule_RemovedFromBeginning]<!--/$RuleNameWithDefaultRule_RemovedFromBeginning-->.
<!--/issueDescription-->

## **Recommended Steps**

If the access control (security rules) result is not desired, view the [Effective Security Rules](https://docs.microsoft.com/azure/virtual-network/virtual-network-nsg-troubleshoot-portal) to determine if the addition or modification of a customer-defined security rule is required. If this traffic should be allowed outbound, create a <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> basic rule specifying port <!--$DestinationPort-->[DestinationPort]<!--/$DestinationPort--> and action Allow.
