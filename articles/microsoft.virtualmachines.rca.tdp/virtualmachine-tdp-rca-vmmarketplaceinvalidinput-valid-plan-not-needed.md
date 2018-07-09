<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - vmmarketplaceinvalidinput-valid-plan-not-needed"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-vmmarketplaceinvalidinput-valid-plan-not-needed"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to the deployment having a plan associated and not requiring the association. 
<!--/issueDescription-->

To work around this issue, please remove from your deployment the marketplace plan information.<br>

To learn more about deploying an image with Marketplace terms:<br>
* [Deploy an image with Marketplace terms and plan information](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage#deploy-an-image-with-marketplace-terms)
