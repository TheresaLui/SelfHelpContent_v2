<properties
pageTitle="LoadBalancer"
description="LoadBalancer"
infoBubbleText="LoadBalancer"
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
displayOrder=""
articleId="CantRDP_LoadBalancer"
diagnosticScenario="LoadBalancer"
selfHelpType="Diagnostic"
supportTopicIds=
resourceTags="windows"
productPesIds=
cloudEnvironments="Public"
/>
# Connectivity Diagnostics Result

<!--issueDescription-->
Microsoft Azure has identified <!--$StatelfulAction-->[StatelfulAction]<!--/$StatelfulAction--> action <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic because the source is the Azure Load Balancer service. This rule is static in the Azure platform to allow the Azure Load Balancer service to communicate with VMs.
1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account.
2. Click Browse > Network Interface.
3. Select the Network Interface of your VM
4. Click on the *Effective routes* blade
5. Modify the appropriate rule which is likely due to setting the destination IP address as an address in the Virtual Network.
 <br>
<!--/issueDescription-->
