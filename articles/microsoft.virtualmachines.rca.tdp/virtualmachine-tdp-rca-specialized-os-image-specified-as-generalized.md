﻿<properties
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
	cloudEnvironments="public"
/>
#We detected a recent issue with your deployment attempt:

<!--issueDescription-->
We identified that your deployment failed for <!--$vmname-->Virtual machine<!--/$vmname-->:** at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. Provisioning of this image failed. One common cause is that the image was configured as generalized but the VM was deployed as specialized. Alternatively, the image was configured as specialized but the VM was deployed as generalized.
<!--/issueDescription-->

Please deploy with both as generalized or both as specialized. Additionally, please review the below documentation on specialized and generalized images.<br>

To learn more about generalized and specialized VMs for **Windows**:<br>
* [Learn how to use a generalized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-generalized-managed)<br>
* [Learn how to use a specialized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized)<br>
* [Learn how to generalize your Windows VM and create an image from it.](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)<br>
* [Learn how to prepare a Windows VHD or VHDx to upload to Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image)<br>

To learn more about generalized and specialized VMs for **Linux**:<br>
* [Learn how to use a generalized image](https://docs.microsoft.com/azure/virtual-machines/linux/capture-image)<br>
* [Learn how to use a specialized image](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.