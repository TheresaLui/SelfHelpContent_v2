	<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-boot-failure-generic"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-boot-failure-generic"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** encountered an issue during booting the VM. At this time, we are unable to determine a specific issue.
<!--/issueDescription-->

To take advantage of additional insights that may offer an RCA when opening a support ticket, please redeploy the VM with boot diagnostics enabled. When boot diagnostics is enabled and telemetry provides an RCA, you will be offered the RCA when opening the ticket.

For common boot errors 
instructions https://docs.microsoft.com/en-us/azure/virtual-machines/linux/boot-diagnostics#common-boot-errors
https://docs.microsoft.com/en-us/azure/virtual-machines/linux/boot-diagnostics#common-boot-errors

](https://docs.microsoft.com/azure/virtual-machines/windows/boot-diagnostics#enable-diagnostics-on-a-new-virtual-machine). When the VM fails provisioning, additional telemetry will be analzyed to determine the reason for the failure.
https://docs.microsoft.com/en-us/azure/virtual-machines/linux/boot-diagnostics#common-boot-errors
To learn more about common boot failures for **Windows**, read (https://docs.microsoft.com/en-us/azure/virtual-machines/windows/boot-diagnostics#common-boot-errors

* [Learn how to prepare a Windows VHD to upload to Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image)<br>
* [Learn how to use a specialized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized)<br>
* [Learn how to use a generalized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-generalized-managed)<br>
* [Learn how to generalize your Windows VM and create an image from it.](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)<br>

To learn more about generalized and specialized VMs for **Linux**:<br>

* [Learn how to use a generalized image](https://docs.microsoft.com/azure/virtual-machines/linux/capture-image)<br>
* [Learn how to use a specialized image](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>
