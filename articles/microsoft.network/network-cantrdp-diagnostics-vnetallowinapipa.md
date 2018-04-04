<properties
pageTitle="VnetAllowInAPIPA"
description="VnetAllowInAPIPA"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
displayOrder=""
articleId="CantRDP_VnetAllowInAPIPA"
diagnosticScenario="VnetAllowInAPIPA"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public"
/>
# We ran connectivity diagnostics on your resource and found an issue.

<!--issueDescription-->
Microsoft Azure has identified <!--$StatefulAction-->[StatefulAction]<!--/$StatefulAction--> action <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic because the source is APIPA. This rule is static in the Azure platform to allow the APIPA address as a source for traffic to VMs and cannot be changed.
 <br>
<!--/issueDescription-->
