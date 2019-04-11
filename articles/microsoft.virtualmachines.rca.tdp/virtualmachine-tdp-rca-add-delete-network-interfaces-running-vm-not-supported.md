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
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of an attempt to delete or add a network interface while the VM was running.
<!--/issueDescription-->
To avoid this issue, first stop the virtual machine before updating interfaces.<br>

You can delete (detach) a network interface only when VM is not running. If a network interface is attached to a VM, you must first place the VM in the stopped (deallocated) state, then delete it from the VM. 

The same is true for adding (attaching) a network interface to a VM.

For guidance on working with network interfaces, see [Add network interfaces to or remove network interfaces from virtual machines](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm).