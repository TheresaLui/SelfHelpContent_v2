<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-hyper-v-driver-did-not-present"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-hyper-v-driver-did-not-present"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because a DVD drive wasn't presented to the VM. This issue is commonly caused when an older Linux kernel is installed or the Linux Integration Service drivers are not installed or outdated.
<!--/issueDescription-->

We recommend that you update any custom images that may be used in future deployments to avoid this issue. If this is a Marketplace image, we recommend reaching out to the publisher directly.<br>

For additional information, please read these additional documents:<br>
* To understand the minimum kernel versions required for a Linux VM in Azure, [please read this article](https://support.microsoft.com/help/4041171).<br>
* To understand the minimum Linux Integration Service (LIS) drivers required, follow the directions in [this article](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic#linux-kernel-requirements).<br>

