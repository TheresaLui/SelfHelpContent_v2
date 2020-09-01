<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - vmsizedoesntsupportpremiumstorage"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-vmsizedoesntsupportpremiumstorage"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because storage account type 'Premium_LRS' is not supported for the VM size specified.
<!--/issueDescription-->

When creating and deploying the virtual machine, verify that the size specified matches the storage account type for Premium Storage.<br>

* To learn more about Premium Storage, read the following articles for [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage) and [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage).
* For information about VM types and sizes in Azure for Windows, see [Windows VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes).<br>
* For information about VM types and sizes in Azure for Linux, see [Linux VM sizes](https://docs.microsoft.com/azure/virtual-machines/linux/sizes).
