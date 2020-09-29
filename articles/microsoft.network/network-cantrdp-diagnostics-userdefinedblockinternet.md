<properties
pageTitle="Route Blocked Internet"
description="Route Blocked Internet"
infoBubbleText="Issues with network traffic were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="CantRDP_BlockInternet"
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
Microsoft Azure has identified an issue which is preventing you from being able to remote into your VM, **<!--$vmname-->[vmname]<!--/$vmname-->**. Access Control **<!--$StatefulAction-->[StatefulAction]<!--/$StatefulAction-->** this **<!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection-->** traffic by customer-defined security rule: **<!--$RuleNameWithDefaultRule_RemovedFromBeginning-->[RuleNameWithDefaultRule_RemovedFromBeginning]<!--/$RuleNameWithDefaultRule_RemovedFromBeginning-->**
<!--/issueDescription-->

## **Recommended Steps**

If the access control (security rules) result is not desired, view the [Effective Security Rules](https://docs.microsoft.com/azure/virtual-network/virtual-network-nsg-troubleshoot-portal) to determine the customer-defined security rule requiring modification. If this traffic should be allowed, create a **<!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection-->** basic rule with a higher priority (lower number) than existing rules specifying **port <!--$DestinationPort-->[DestinationPort]<!--/$DestinationPort-->**. If this traffic should not be allowed, create a **<!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection-->** advanced rule with a higher priority (lower number) than existing rules specifying the source and destination IPs desired, **port <!--$DestinationPort-->[DestinationPort]<!--/$DestinationPort-->**, and action Deny.
