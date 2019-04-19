<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - sku promotion expired"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-blocknewsubcription-promo-expired"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds=""
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the  promotional SKU **<!--$SkuPromo-->SKU promo<!--/$SkuPromo-->** associated with this subscription has expired. This VM can no longer be deployed.<br>
<!--/issueDescription-->

Thank you for participating in the **<!--$SkuPromo-->SKU promo<!--/$SkuPromo-->**. Now that this promotion has expired, we invite you to use the **<!--$SkuStandard-->standard SKU<!--/$SkuStandard-->** for the disk configuration that was provided in the promotional offer.<br>

For a list of our current offers, see [Microsoft Azure Offer Details](https://azure.microsoft.com/support/legal/offer-details/).


