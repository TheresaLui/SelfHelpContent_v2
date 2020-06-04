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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because you are trying to use **<!--$SkuPromo-->SKU promo<!--/$SkuPromo-->** that is a **limited** promotional SKU that's unavailable at this time. This specific VM with this SKU can no longer be deployed.<br>
<!--/issueDescription-->

Please find a suitable SKU size that meets your deployment needs. For a list of our current offers, see [Microsoft Azure Offer Details](https://azure.microsoft.com/support/legal/offer-details/).<br>

For an overview of Azure VM sizes, see the following:

- [Sizes for Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sizes)
- [Sizes for Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/sizes)
- [Resource SKUs - Available VM sizes for a subscription](https://docs.microsoft.com/rest/api/compute/resourceskus/list).


