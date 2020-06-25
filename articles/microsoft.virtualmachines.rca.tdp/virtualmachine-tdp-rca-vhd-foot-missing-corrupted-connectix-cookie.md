<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-vhd-foot-missing-corrupted-connectix-cookie"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-vhd-foot-missing-corrupted-connectix-cookien"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to a problem with the VHD file. The problem can be caused by one of the following:<br>

1. The VHD does not comply with the 1 MB alignment (offset). The supported disk size should be 1 MB * N. For example, the disk should be 102,401 MB.
2. The VHD is corrupted.
<!--/issueDescription-->

For additional information and how to mitigate, please read the following [KB article](https://support.microsoft.com/help/4053292).<br>

To learn more about how to prepare and upload images to Azure, please follow these instructions for [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) and [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic).<br>
