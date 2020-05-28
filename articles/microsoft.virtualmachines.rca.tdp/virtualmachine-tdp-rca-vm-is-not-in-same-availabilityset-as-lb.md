<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-vm-is-not-in-same-availabilityset-as-lb"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-vm-is-not-in-same-availabilityset-as-lb"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because a load balancer has been configured but the load balancer is not in the same availability set as the virtual machine being deployed.
<!--/issueDescription-->

Possible solutions:<br>

1. Move the VM into an availability set that the load balancer is configured for.<br>
2. [Combine a load balancer with availability sets](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>

For additional information regarding load balancers, please read the following document:<br>

* [What is Azure Load Balancer?](https://docs.microsoft.com/azure/load-balancer/load-balancer-overview)
* [Using Azure Resource Manager Support with Azure Load Balancer](https://docs.microsoft.com/azure/load-balancer/load-balancer-arm)<br>

For additional ARM template examples, please review the following templates:<br>

* [Load Balancer with two VIPs, each with one LB rule](https://azure.microsoft.com/resources/templates/101-loadbalancer-with-multivip/)<br>
* [Two VMs in VNET - Internal Load Balancer and LB rules](https://azure.microsoft.com/resources/templates/201-2-vms-loadbalancer-lbrules/)
