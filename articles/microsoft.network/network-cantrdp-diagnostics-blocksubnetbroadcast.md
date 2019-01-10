<properties
pageTitle="BlockSubnetBroadcast"
description="BlockSubnetBroadcast"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
displayOrder=""
articleId="CantRDP_BlockSubnetBroadcast"
diagnosticScenario="BlockSubnetBroadcast"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public"
/>
# We ran connectivity diagnostics on your resource and found an issue.

<!--issueDescription-->
Microsoft Azure has identified <!--$StatefulAction-->[StatefulAction]<!--/$StatefulAction--> action <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic is a broadcast to the subnet. Sending broadcast traffic is not supported in the Azure Platform. It cannot be enabled. More details [here](https://docs.microsoft.com/azure/virtual-network/virtual-networks-faq).
 <br>
<!--/issueDescription-->
