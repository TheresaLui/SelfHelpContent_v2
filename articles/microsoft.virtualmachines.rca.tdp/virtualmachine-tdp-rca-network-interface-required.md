<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - VM must have at least one network interface"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-network-interface-required"
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
The operation on virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the  Azure virtual machine must have at least one network interface. An attempt was made to detach a network interface from a VM when it is the only attached network interface. A virtual machine must have at least one network interface attached to it at all times.
<!--/issueDescription-->

## **Recommended Steps**

You can detach a network interface from a VM provided it has at least one other network interface attached to it. You can delete a network interface from a VM's networking provided that it not attached to the VM.

For guidance on working with network interfaces, see [Add network interfaces to or remove network interfaces from virtual machines](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm).
