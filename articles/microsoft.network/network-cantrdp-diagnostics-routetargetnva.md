<properties
pageTitle="Route Target NVA"
description="Route Target NVA"
infoBubbleText= "Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
ms.author="chadmat"
displayOrder=""
articleId="CantRDP_RouteTargetNVA"
diagnosticScenario="Route Target NVA"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran connectivity diagnostics on your resource and found an issue

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. We identified that this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic is <!--$StatelessAction-->[StatelessAction]<!--/$StatelessAction--> to route via a Network Virtual Appliance (NVA). If the routing result is not desired, view the Effective Route Table to determine the User Defined Route (UDR) configuration pointing the next hop to the NVA. For routing issues at the NVA, review the NVA configuration to determine the routing path for this traffic.
<!--/issueDescription-->

## **Recommended Steps**

1. From a browser, navigate to http://portal.azure.com and, if necessary, sign in with your Azure account
2. Click Browse > Network Interface
3. Select the Network Interface of your VM
4. Click on the *Effective routes* blade
5. Modify the appropriate rule which is likely due to setting the destination IP address as an address in the Virtual Network
