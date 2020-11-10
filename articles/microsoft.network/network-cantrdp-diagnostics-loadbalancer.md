<properties
pageTitle="LoadBalancer"
description="LoadBalancer"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="CantRDP_LoadBalancer"
diagnosticScenario="LoadBalancer"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>

# We ran connectivity diagnostics on your resource and found an issue

<!--issueDescription-->
Microsoft Azure has identified <!--$StatefulAction-->[StatefulAction]<!--/$StatefulAction--> action <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic because the source is the Azure Load Balancer service. This rule is static in the Azure platform to allow the Azure Load Balancer service to communicate with VMs.
<!--/issueDescription-->


## **Recommended Steps**

1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account
2. Click Browse > Network Interface
3. Select the Network Interface of your VM
4. Click on the *Effective routes* blade
5. Modify the appropriate rule which is likely due to setting the destination IP address as an address in the Virtual Network
