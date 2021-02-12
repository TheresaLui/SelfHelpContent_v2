<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - Specialized OS image specified as generalized"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachinescalesets"
	authors="summertgu"
	ms.author="tiag"
	displayOrder=""
	articleId="VMSS_DeploymentFailure_RCA-specialized_os_image_specified_as_generalized"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32641079,32641082,32641076,32641075,32641080,32641074,32641076,32641077,32641072,32641073"
	resourceTags=""
	productPesIds="16080"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine scale set **<!--$vmssname-->Virtual machine scale set<!--/$vmssname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** encountered an issue due to the custom VM image not being provisioned correctly. One common cause is that the custom VM image was configured as specialized but the VM scale set was deployed as generalized. Creating a VM scale set from a specialized VHD is not supported.
<!--/issueDescription-->

Please configure the image and deploy the VM scale set as generalized [(Reference)](https://docs.microsoft.com/azure/virtual-machine-scale-sets/tutorial-use-custom-image-powershell#create-a-scale-set-from-the-custom-vm-image). Additionally, please review the below documentation on specialized and generalized images.<br>

To learn more about generalized and specialized VMs for **Windows**:<br>

* [Learn how to prepare a Windows VHD to upload to Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image)<br>
* [Learn how to use a specialized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized)<br>
* [Learn how to use a generalized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-generalized-managed)<br>
* [Learn how to generalize your Windows VM and create an image from it.](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)<br>

To learn more about generalized and specialized VMs for **Linux**:<br>

* [Learn how to use a generalized image](https://docs.microsoft.com/azure/virtual-machines/linux/capture-image)<br>
* [Learn how to use a specialized image](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>
