<properties
pageTitle="No Route from Internet"
description="No Route from Internet"
infoBubbleText="Issues with network traffic were detected. See details on the right."
service="microsoft.network"
resource="virtualnetworks"
authors="chadmath"
ms.author="chadmat"
displayOrder=""
articleId="CantRDP_NoRouteFromInternet"
diagnosticScenario="Internet traffic"
selfHelpType="Diagnostics"
supportTopicIds="32511135, 32411835, 32584250, 32584252"
resourceTags="windows"
productPesIds="16342, 14745, 15571, 15797, 14749, 15526"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_VirtualNetwork"
/>

# We ran connectivity diagnostics on your resource and found an issue

<!--issueDescription-->
Microsoft Azure has identified an issue which is preventing you from being able to remote into your VM, **<!--$vmname-->[vmname]<!--/$vmname-->**. Routing **<!--$action-->[action]<!--/$action-->**  this **<!--$TrafficDirection-->[TrafficDirection]<!--/$TrafficDirection-->** traffic because there are not any routes defined for internet routable IPs.
<!--/issueDescription-->

## **Recommended Steps**

If the routing result is not desired, check to ensure the VM is associated with a [public IP address](https://docs.microsoft.com/azure/virtual-network/virtual-network-deploy-static-pip-arm-portal?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) either directly on a NIC IPConfig, or as a member of a Azure Load Balancer backend address pool.
