<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - disk wrong type - invalidvhd"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-disk-wrong-type-invalidvhd"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to VHD not being of the type fixed disk. The VHD has been detected to be of the type dynamic or differencing.
<!--/issueDescription-->

To find out more about VHDs and how Azure only supports the fixed disk VHD format, read the following articles [for Windows](https://docs.microsoft.com/azure/virtual-machines/windows/about-disks-and-vhds?toc=%2Fazure%2Fvirtual-machines%2Fwindows%2Ftoc.json#about-vhds) and [for Linux](https://docs.microsoft.com/azure/virtual-machines/linux/about-disks-and-vhds?toc=%2Fazure%2Fvirtual-machines%2Flinux%2Ftoc.json#about-vhds).<br>

For specific instructions on how to convert a dynamic or differencing disk to the type fixed, please read [this article for windows](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image#convert-the-virtual-disk-to-vhd-and-fixed-size-disk) and [this article for linux](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic#general-linux-installation-notes).<br>

To learn more about how to prepare a VHD before uploading the image to azure, read the following articles for [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image) and [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic).<br>
