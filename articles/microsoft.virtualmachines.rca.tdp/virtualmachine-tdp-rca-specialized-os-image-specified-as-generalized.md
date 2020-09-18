<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - Specialized OS image specified as generalized"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-specialized_os_image_specified_as_generalized"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** encountered an issue due to the image not being provisioned correctly. One common cause is that the image was configured as specialized but the VM was deployed as generalized.
<!--/issueDescription-->

Please configure the image and deploy the VM with the same method (both as generalized or both as specialized). Additionally, please review the below documentation on specialized and generalized images.<br>

To learn more about generalized and specialized VMs for **Windows**:<br>

* [Learn how to prepare a Windows VHD to upload to Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image)<br>
* [Learn how to use a specialized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized)<br>
* [Learn how to use a generalized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-generalized-managed)<br>
* [Learn how to generalize your Windows VM and create an image from it.](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)<br>

To learn more about generalized and specialized VMs for **Linux**:<br>

* [Learn how to use a generalized image](https://docs.microsoft.com/azure/virtual-machines/linux/capture-image)<br>
* [Learn how to use a specialized image](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>
