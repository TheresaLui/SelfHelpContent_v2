<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - add or delete networking interfaces on running VM not supported"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-add-delete-network-interfaces-running-vm-not-supported"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The operation on virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of an attempt to attach or detach a network interface while the VM was running.
<!--/issueDescription-->
To avoid this issue, first stop the virtual machine before changing network interfaces.<br>

You can attach or detach a network interface only when the VM is in a deallocated state (stopped). 

For guidance on working with network interfaces, see [Add network interfaces to or remove network interfaces from virtual machines](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm).