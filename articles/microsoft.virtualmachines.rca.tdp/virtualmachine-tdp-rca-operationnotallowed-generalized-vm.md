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
	cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because starting a generalized VM is not supported.
<!--/issueDescription-->

A generalized VM is a virtual machine with personal account information removed so that its image can be used for creating other VMs. You also might get this error if you are attempting to start the VM after it was captured.<br> 

There is no way to return the VM that generated this error back to its original state as a functioning virtual machine, but you can do one of the following:

- If you have the image that you used to create the original VM, you can use that image to create a new VM.
- Replace the VM by recreating it from an existing VHD.
- If you have a VHD that contains the user accounts, applications, and other state data from your original VM, you can create a new VM by attaching that disk as the OS disk.<br>

See the following documents for help with your deployments:

- [Create a managed image of a generalized VM in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-classic-capture-image/)
- [Create an unmanaged VM image from an Azure VM](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-capture-image)
- [Upload a generalized VHD and use it to create new VMs in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-upload-image)
- [Create a Windows VM from a specialized disk by using PowerShell](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-create-vm-specialized/)


