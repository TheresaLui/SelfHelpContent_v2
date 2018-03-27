<properties
pageTitle="UserRule1"
description="UserRule1"
infoBubbleText= "Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
displayOrder=""
articleId="CantRDP_RouteTargetVNet"
diagnosticScenario="Running VM attached"
selfHelpType="Diagnostic"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public"
/>
# We ran connectivity diagnostics on your resource and found an issue.

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. We identified that this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic is <!--$StatelfulAction-->[StatelfulAction]<!--/$StatelfulAction--> by security rule: <!--$RuleNameWithUserRule_RemovedFromBeginning-->[RuleNameWithUserRule_RemovedFromBeginning]<!--$RuleNameWithUserRule_RemovedFromBeginning-->. 
<!--/issueDescription-->
If the security rules result is not desired, view the [Effective Security Rules](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-nsg-troubleshoot-portal) to view and modfiy the rule. If this traffic should be allowed, create a $TrafficDirection basic rule with a higher priority (lower number) than existing rules specifying port $port. If this traffic should not be allowed, create a $TrafficDirection advanced rule with a higher priority (lower number) than existing rules specifying the source and destination IPs desired, port $port, and action Deny.
1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account.
2. Click Browse > Network Securtiy Groups.
3. Select the Network Interface of your VM
4. Click on the *Effective routes* blade
5. Modify the appropriate rule which is likely due to setting the destination IP address as an address in the Virtual Network.
 <br>

