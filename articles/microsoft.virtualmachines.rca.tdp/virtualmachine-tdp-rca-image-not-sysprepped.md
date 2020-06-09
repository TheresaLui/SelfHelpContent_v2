<properties
	pageTitle="Deployment Failure RCA"
	description="RCA image-not-sysprepped"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-image-not-sysprepped"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows"
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to issues with the guest getting a DHCP address. One common cause is that the image did not have 'sysprep' correctly run.
<!--/issueDescription-->

## When to use Sysprep
Sysprep is a process that is run where  windows installation will reset the installation of the system and will provide an “out of the box experience” by removing all personal data and resetting several components. For details about Sysprep, see [How to Use Sysprep: An Introduction.](http://technet.microsoft.com/library/bb457073.aspx) for instructions on how to generalize an image.

To learn more about generalized and specialized VMs for **Windows**:<br>

* [Learn how to prepare a Windows VHD to upload to Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image)<br>
* [Learn how to use a specialized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized)<br>
* [Learn how to use a generalized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-generalized-managed)<br>
* [Learn how to generalize your Windows VM and create an image from it.](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)<br>

Once the original image has been fixed to have Sysprep properly completed, remember to update the image in Azure being referenced for the deployment.

If this is a Marketplace image, we recommend reaching out to the publisher directly.<br>
