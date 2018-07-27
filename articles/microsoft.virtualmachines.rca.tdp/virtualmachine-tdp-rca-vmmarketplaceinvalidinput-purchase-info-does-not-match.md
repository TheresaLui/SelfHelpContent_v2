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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the plan information specified during deployment was configured but does not match with what was expected for that image during the validation phase.
<!--/issueDescription-->

A Marketplace image, or an image associated to a publisher, in Azure has the following attributes:

| Term 				  | Definition    |
|:-------------:|-------------	|
| Publisher 		| The organization that created the image. Examples: Canonical, MicrosoftWindowsServer |
|  Offer        |  Name of a group of related images created by a publisher. Examples: Ubuntu Server, WindowsServer |
| SKU 					| An instance of an offer, such as a major release of a distribution. Examples: 16.04-LTS, 2016-Datacenter |
|  Version 			|The version number of an image SKU|

To view an image's purchase plan information, run  [*Get-AzureRMVMImage*](https://docs.microsoft.com/powershell/module/azurerm.compute/get-azurermvmimage)(PS) or [*az vm image show *](https://docs.microsoft.com/cli/azure/image#az_image_show)(CLI) to obtain the above properties.

Example:<br>

	$version = "2016.127.20170406"
	Get-AzureRMVMImage -Location $locName -Publisher $pubName -Offer $offerName -Skus $skuName -Version $version

Once the properties have been identified, validate  your configuration for the deployment and compare the results. Often, there is a typo or the plan no longer exists. When no longer existing, please reach out to the publisher support channel for assistance or select a new plan/image to deploy.<br>

Example:<br>

	PurchasePlan : {
         "publisher": "microsoft-ads",
         "name": "windows2016",
         "product": "windows-data-science-vm"

To learn more about deploying an image with Marketplace terms and plan:<br>

* To understand how to configure Marketplace plan information correctly or without,  [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage#view-plan-properties) and [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage#view-plan-properties)<br>
* Learn more about how to set Marketplace plan information [via the ARM API](https://docs.microsoft.com/rest/api/compute/virtualmachines/createorupdate#plan)

Additional Info:<br>

If the image publisher provides additional license and purchase terms, you must accept those terms and enable programmatic deployment. You also need to supply purchase plan parameters when deploying a VM programmatically. See Deploy an image with Marketplace terms.<br>

To *accept the publisher terms*, refer to the [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage#accept-the-terms) and [Linux](https://docs.microsoft.com/azure/virtual-machines/linuxs/cli-ps-findimage#accept-the-terms) documentation.<br>
