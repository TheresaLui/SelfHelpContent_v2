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
	resourceTags="windows"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>

# Operation not allowed on generalized Virtual Machine

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because starting a generalized VM is not supported.
<!--/issueDescription-->

A generalized VM is a virtual machine with personal account information removed so that its image can be used for creating other VMs. You also might get this error if you are attempting to start the VM after it was captured.<br> 

There is no way to return the VM that generated this error back to its original state as a functioning virtual machine; however the following options may be helpful depending on your resources:

- Replace the VM by recreating it from the VHD used to create the original VM
- Create a new VM from the image used to create the original VM
- Create a new VM with a VHD that contains the user accounts, applications, and other state data from your original VM. Attach the VHD as the OS disk.<br>

## **Recommended Documents**

- [Create a managed image of a generalized VM in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-classic-capture-image/)
- [Create an unmanaged VM image from an Azure VM](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-capture-image)
- [Upload a generalized VHD and use it to create new VMs in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-upload-image)
- [Create a Windows VM from a specialized disk by using PowerShell](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-create-vm-specialized/)


