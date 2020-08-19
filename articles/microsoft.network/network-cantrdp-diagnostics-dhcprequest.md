<properties
pageTitle="DhcpRequest"
description="DhcpRequest"
infoBubbleText= "Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="CantRDP_DhcpRequest"
diagnosticScenario="DhcpRequest"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>

# We ran connectivity diagnostics on your resource and found an issue

<!--issueDescription-->
Microsoft Azure has identified <!--$StatefulAction-->[StatefulAction]<!--/$StatefulAction--> action <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic because the destination is used for VMs to send DHCP requests. This rule is static in the Azure platform to allow VMs to request DHCP configuration and cannot be changed.
<!--/issueDescription-->
