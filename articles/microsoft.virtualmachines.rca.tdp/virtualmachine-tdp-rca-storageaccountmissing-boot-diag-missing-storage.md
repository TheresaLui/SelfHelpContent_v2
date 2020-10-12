<properties
	pageTitle="Start Failure RCA"
	description="RCA - storageaccountmissing-boot-diag-missing-storage"
	infoBubbleText="Found recent start failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-storageaccountmissing-boot-diag-missing-storage"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics and found an issue

<!--issueDescription-->
We have detected a start operation for the virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the boot diagnostics storage account could not be found.
<!--/issueDescription-->

To mitigate the issue update the boot diagnostics settings to use an alternative storage account <br>

For more information about boot diagnostics, see the below articles:
* [Windows VM Boot Diagnostics](https://docs.microsoft.com/azure/virtual-machines/windows/boot-diagnostics)
* [Linux VM Boot Diagnostics](https://docs.microsoft.com/azure/virtual-machines/linux/boot-diagnostics)<br>
