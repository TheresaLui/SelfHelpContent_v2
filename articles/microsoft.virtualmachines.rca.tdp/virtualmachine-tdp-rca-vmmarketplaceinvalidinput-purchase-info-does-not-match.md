<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - vmmarketplaceinvalidinput-purchase-info-does-not-match"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-vmmarketplaceinvalidinput-purchase-info-does-not-match"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to the plan information specified during deployment was configured but does not match with what was expected for that image.
<!--/issueDescription-->

To learn more about deploying an image with Marketplace terms and plan:<br>
* Understanding how to configure Marketplace plan information correctly for [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage#deploy-an-image-with-marketplace-terms) and [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage#deploy-an-image-with-marketplace-terms)<br>
* Learn more about how to set Plan Information [via the ARM API](https://docs.microsoft.com/rest/api/compute/virtualmachines/createorupdate#plan)
