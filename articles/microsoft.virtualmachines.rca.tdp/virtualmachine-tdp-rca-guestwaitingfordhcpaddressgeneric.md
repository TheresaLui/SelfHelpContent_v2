<properties
	pageTitle="Deployment Failure RCA"
	description="RCA-guestwaitingfordhcpaddress"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-guestwaitingfordhcpaddress"	
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to issues with the guest getting a DHCP address. One common cause is that the image was configured improperly.
<!--/issueDescription-->

Before creating or uploading a Windows virtual machine image, review the [documentation](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image#check-the-windows-services) to learn how to enable and configure services before uploading the image.<br>

For Linux virtual machines, verify that you have followed the documentation before [creating and uploading the image](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic) or [capturing the image.](https://docs.microsoft.com/azure/virtual-machines/linux/capture-image)<br>

We recommend that you update any custom images that may be used in future deployments to avoid this issue.
