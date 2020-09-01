<properties
pageTitle="VnetWideOpenCnet"
description="VnetWideOpenCnet"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="CantRDP_VnetWideOpenCnet"
diagnosticScenario="VnetWideOpenCnet"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>
# We ran connectivity diagnostics on your resource and found an issue

<!--issueDescription-->
Microsoft Azure has identified <!--$StatefulAction-->[StatefulAction]<!--/$StatefulAction--> action <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic because the destination is in the Virtual Network, peered Virtual Network, or local network address space.
<!--/issueDescription-->

## **Recommended Steps**

If this is not desired, create a Network Security Group defining only the traffic you wish to allow and associate it to the Virtual Machine’s network interface as documented [here](https://docs.microsoft.com/azure/virtual-network/virtual-networks-create-nsg-arm-pportal).
