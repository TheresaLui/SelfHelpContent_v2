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
We detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because you are trying to use **<!--$SkuPromo-->SKU promo<!--/$SkuPromo-->** that is a **limited** promotional SKU that's unavailable at this time. This specific VM with this SKU can no longer be deployed.<br>
<!--/issueDescription-->

Thank you for trying your deployment with **<!--$SkuPromo-->promo SKU<!--/$SkuPromo--> SKU**. Now that this promotion has expired, we invite you to use the **<!--$SkuStandard-->standard SKU<!--/$SkuStandard--> SKU** which is of comparable specification to the promotional one.<br>

For a list of our current offers, see [Microsoft Azure Offer Details](https://azure.microsoft.com/support/legal/offer-details/).<br>

For an overview of Azure VM sizes, see the following:
- [Sizes for Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sizes)
- [Sizes for Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/sizes)<br>

For a list of available VM sizes for a subscription, see [Resource SKUs](https://docs.microsoft.com/rest/api/compute/resourceskus/list).


