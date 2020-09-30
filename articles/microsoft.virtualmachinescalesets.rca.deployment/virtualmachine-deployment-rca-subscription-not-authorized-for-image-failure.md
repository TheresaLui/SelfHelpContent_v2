<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - subscription-not-authorized-for-image-failure"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachinescalesets"
	authors="summertgu"
	ms.author="tiag"
	displayOrder=""
	articleId="VMSS_DeploymentFailure_rca-subscription-not-authorized-for-image-failure"
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
We have detected that the deployment for virtual machine scale set **<!--$vmssname-->Virtual machine scale set<!--/$vmssname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to the subscription not being authorized for the image. Either the specified image is no longer available, marked as private (test), or the image may only be available for MSDN or EA customers.
<!--/issueDescription-->

To work around this issue, validate that the specific image is available to your subscription and the specific version is available.<br>

To learn more about different ways to find information for an image:
* [How to find information for an image](https://docs.microsoft.com/azure/virtual-machines/windows/overview#operating-system-disks-and-images)
