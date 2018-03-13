<properties
pageTitle="VnetWideOpenInternet"
description="VnetWideOpenInternet"
infoBubbleText="VnetWideOpenInternet"
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
displayOrder=""
articleId="CantRDP_VnetWideOpenInternet"
diagnosticScenario="VnetWideOpenInternet"
selfHelpType="diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="public"
/>
# Connectivity Diagnostics Result

<!--issueDescription-->
Microsoft Azure has identified <!--$StatelfulAction-->[StatelfulAction]<!--/$StatelfulAction--> action <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic because the destination is the Internet and no Network Security Group has been configured to block it. If this is not desired, create a Network Security Group defining only the traffic you wish to allow and associate it to the Virtual Machine’s network interface as documented [here](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-create-nsg-arm-pportal).
 <br>
<!--/issueDescription-->