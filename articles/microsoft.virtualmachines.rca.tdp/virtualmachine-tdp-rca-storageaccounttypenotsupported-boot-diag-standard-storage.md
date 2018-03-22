<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - storageaccounttypenotsupported-boot-diag-standard-storage
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-storageaccounttypenotsupported-boot-diag-standard-storage"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public"
/>
# We ran diagnostics and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the deployment had boot diagnostics enabled using a premium storage account.
<!--/issueDescription-->

When creating and deploying the virtual machine, verify that the storage account being used for boot diagnostics is standard storage. If multiple storage accounts are available, the action can default to using a storage account that is not of type standard.<br>

For information about how to use boot diagnostics to troubleshoot virtual machines in Azure, see [Windows VM Boot Diagnostics](https://docs.microsoft.com/azure/virtual-machines/windows/boot-diagnostics). For information specific to Linux, see [Linux VM Boot Diagnostics](https://docs.microsoft.com/azure/virtual-machines/linux/boot-diagnostics).<br>
