<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - Operation not allowed on generalized VM"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_rca-OperationNotAllowedOnGeneralizedVM"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds=""
	cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because starting a VM from a generalized image is not supported.
<!--/issueDescription-->

To work with generalized images correctly, follow this process:

- Generalize the VM by running `sysprep`.
- Deallocate the resources in the VM.
- Set the VM state to generalized.
- Create the image.
- Create the VM from the image.

For instructions, see [How to create an unmanaged VM image from an Azure VM](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-capture-image).

Alternatively, if you have disk image that contains the user accounts, applications, and other state data from your original VM, you can create a new VM by attaching that specialized managed disk as the OS disk. For more information, see [Create a Windows VM from a specialized disk by using PowerShell](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-create-vm-specialized/).

See also:

- [Upload a generalized VHD and use it to create new VMs in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-upload-image)
- [Create a managed image of a generalized VM in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-classic-capture-image/)

