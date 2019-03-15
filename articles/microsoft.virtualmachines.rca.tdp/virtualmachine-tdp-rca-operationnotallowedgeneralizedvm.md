<properties
	pageTitle="VM start not allowed on generalized VM"
	description="RCA - start not allowed on generalized VM"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.authors="scotro"
	displayOrder=""
	articleId="DeploymentFailure_rca-startnotallowedgeneralizedvm"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds=""
	cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because because the VM is generalized. Generalized VMs cannot be started.
<!--/issueDescription-->

If you are using a generalized image that you created from a VM by running `syssprep`, review working with generalized images and creating VMs from them as described in [How to create an unmanaged VM image from an Azure VM](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-capture-image).

If you are not using a generalized image, create a new VM by attaching a specialized managed disk as the OS disk. A specialized disk is a copy of a virtual hard disk (VHD) from an existing VM that contains the user accounts, applications, and other state data from your original VM. For instructions, see [Create a Windows VM from a specialized disk by using PowerShell](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-create-vm-specialized/).

See also:
- [Sysprep (Generalize) a Windows installation](https://docs.microsoft.com/windows-hardware/manufacture/desktop/sysprep--generalize--a-windows-installation)
- [Sysprep process overview](https://docs.microsoft.comwindows-hardware/manufacture/desktop/sysprep-process-overview)
- [Upload a generalized VHD and use it to create new VMs in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-upload-image)
- [Create a managed image of a generalized VM in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-classic-capture-image/)

