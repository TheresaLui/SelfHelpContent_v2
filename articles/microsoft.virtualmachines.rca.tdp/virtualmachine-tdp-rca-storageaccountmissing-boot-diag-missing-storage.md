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
	cloudEnvironments="public"
/>
# We ran diagnostics and found an issue

<!--issueDescription-->
We have detected that the start for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because boot diagnostics storage container could not be found. For most scenarios, the customer has deleted the storage account.
<!--/issueDescription-->

When creating and deploying the virtual machine, verify that the storage account being used for boot diagnostics is not deleted.<br>

For information about how to use boot diagnostics to troubleshoot virtual machines in Azure, see [Windows VM Boot Diagnostics](https://docs.microsoft.com/azure/virtual-machines/windows/boot-diagnostics). For information specific to Linux, see [Linux VM Boot Diagnostics](https://docs.microsoft.com/azure/virtual-machines/linux/boot-diagnostics).<br>
