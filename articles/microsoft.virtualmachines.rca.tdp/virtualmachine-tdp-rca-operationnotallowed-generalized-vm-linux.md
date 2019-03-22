<properties
	pageTitle="Deploymenent Failure RCA"
	description="RCA - Operation not allowed on generalized VM"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_rca-OperationNotAllowedOnGeneralizedVM-Linux"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="linux"
	productPesIds=""
	cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because starting a generalized VM is not supported.
<!--/issueDescription-->

A generalized VM is a virtual  machine with personal account information removed so that its image can be used for creating other VMs. Apparently the original VM was started instead of a VM created from its image. 

You can also get this error if the VM was captured and then restarted, regardless if the VM has been deprovisioned of personal account information. If a generalized VM is mistakenly started, as may be the case with this error, the VM must be deprovisioned again to remove any personal information that may have been saved.

There is no way to return a generalized VM back to its original state as a functioning virtual machine.

You have two options:

- Create an image of the generalized VM. You can then use that image to create another VM. 
- Create a new VM using a specialized disk. 

## Create an image of the generalized VM

According to your scenario, perform the following steps to deploy a VM based on the image of the original VM.

1. Generalize the VM by running this bash command: `sudo waagent -deprovision+user`
1. Deallocate the resources in the VM.
1. Set the VM state to generalized.
1. Create the image.
1. Create the VM from the image.

For instructions, see [How to create an unmanaged VM image from an Azure VM](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-capture-image).

## Create a new VM from a specialized disk

If you have a disk image that contains the user accounts, applications, and other state data from your original VM, you can create a new VM by attaching that disk as the OS disk. For more information, see [Create a Windows VM from a specialized disk by using PowerShell](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-create-vm-specialized/).

See also:

- [Upload a generalized VHD and use it to create new VMs in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-upload-image)
- [Create a managed image of a generalized VM in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-classic-capture-image/)

