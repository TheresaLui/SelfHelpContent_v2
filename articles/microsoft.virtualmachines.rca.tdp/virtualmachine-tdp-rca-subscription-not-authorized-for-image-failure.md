<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - subscription-not-authorized-for-image-failure"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
 ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_rca-subscription-not-authorized-for-image-failure"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to the subscription not being authorized for the image. Either the specified image is no longer available, marked as private (test), or the image may only be available for MSDN or EA customers.
<!--/issueDescription-->

To work around this issue, validate that the specific image is available to your subscription and the specific version is available.<br>

To learn more about different ways to find information for an image:
* [How to find information for an image](https://docs.microsoft.com/azure/virtual-machines/windows/overview#operating-system-disks-and-images)
