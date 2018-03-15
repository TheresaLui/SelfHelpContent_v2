<properties
pageTitle="DefaultOutDenyAll"
description="DefaultOutDenyAll"
infoBubbleText="DefaultOutDenyAll"
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
displayOrder=""
articleId="CantRDP_DefaultOutDenyAll"
diagnosticScenario="DefaultOutDenyAll"
selfHelpType="Diagnostic"
supportTopicIds=
resourceTags="windows"
productPesIds=
cloudEnvironments="Public"
/>
# Connectivity Diagnostics Result

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. We identified that this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic is <!--$StatelfulAction-->[StatelfulAction]<!--/$StatelfulAction--> by a default security rule: <!--$RuleNameWithDefaultRule_RemovedFromBeginning-->[RuleNameWithDefaultRule_RemovedFromBeginning]<!--$RuleNameWithDefaultRule_RemovedFromBeginning-->. If the access control (security rules) result is not desired, view the Effective Security Rules to determine if the addition or modification of a customer-defined security rule is required. If this traffic should be allowed outbound, create a <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> basic rule specifying port <!--$DestinationPort-->[DestinationPort]<!--$DestinationPort--> and action Allow.
 <br>
<!--/issueDescription-->
