<properties
pageTitle="Virtual Network Service Endpoint"
description="Virtual Network Service Endpoint"
infoBubbleText="Issues with network traffic routing were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="anavinahar"
displayOrder=""
articleId="CantRDP_ServiceEndpoints"
diagnosticScenario="Service Endpoint"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public"
/>
# We ran connectivity diagnostics on your resource and found an issue.

<!--issueDescription-->
Microsoft Azure has identified a routing issue which is preventing you from being able to remote into your VM, <!--$vmname-->[vmname]<!--/$vmname-->. We identified that this <!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection--> traffic is <!--$StatelessAction-->[StatelessAction]<!--/$StatelessAction--> by Virtual Network Service Endpoint (the traffic stays on the Microsoft Azure backbone network). 
<!--/issueDescription-->
If you do not want traffic to be sent directly to the Azure Service Endpoint, deselect the Azure service from the Virtual Network Subnet as described [here](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoints-configure)
 <br>

