<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - vmmarketplaceinvalidinput-valid-plan-not-needed"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_rca-vmmarketplaceinvalidinput-valid-plan-not-needed"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to the deployment having a Marketplace plan defined when it is not required. Validation within the platform detected the plan information being present.
<!--/issueDescription-->

The deployment does not require the Marketplace plan information and needs to be removed. To work around this issue, please remove from your deployment action the marketplace plan information and redeploy.<br>

A Marketplace image, or an image associated to a publisher, in Azure has the following attributes:<br>

| Term 				  | Definition    |
|:-------------:|-------------	|
| Publisher 		| The organization that created the image. Examples: Canonical, MicrosoftWindowsServer |
|  Offer        |  Name of a group of related images created by a publisher. Examples: Ubuntu Server, WindowsServer |
| SKU 					| An instance of an offer, such as a major release of a distribution. Examples: 16.04-LTS, 2016-Datacenter |
|  Version 			|The version number of an image SKU|

To view an image's purchase plan information, run  [*Get-AzVMImage*](https://docs.microsoft.com/powershell/module/az.compute/get-azvmimage)(PS) or [*az vm image show *](https://docs.microsoft.com/cli/azure/image#az_image_show)(CLI) to obtain the above properties.<br>

Example:<br>

	$version = "2016.127.20170406"
	Get-AzVMImage -Location $locName -Publisher $pubName -Offer $offerName -Skus $skuName -Version $version

*Example:*<br>

			PurchasePlan : {
	           "publisher": "publisher name",
	           "name": "windows2016",
	           "product": "windows-data-science-vm"
					 }

To learn more about deploying an image with Marketplace terms and plan:<br>

* To understand how to configure Marketplace plan information correctly or without,  [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/cli-ps-findimage#view-plan-properties) and [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/cli-ps-findimage#view-plan-properties)<br>
* Learn more about how to set Marketplace plan information [via the ARM API](https://docs.microsoft.com/rest/api/compute/virtualmachines/createorupdate#plan)
