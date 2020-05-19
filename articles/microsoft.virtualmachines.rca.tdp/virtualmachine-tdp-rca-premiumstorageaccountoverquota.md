<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-premiumstorageaccountoverquota"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-premiumstorageaccountoverquota"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to exceeding the total disk capacity for your Premium Storage Account.
<!--/issueDescription-->

To mitigate the issue, please move your image to a Premium Storage Account with fewer VHDs and deploy from there.<br>

To learn more about max limits for Premium Storage Accounts, [please read this article](https://azure.microsoft.com/documentation/articles/storage-premium-storage).<br>

To learn more about scalability and performance targets and limits, please read [this article](https://docs.microsoft.com/azure/storage/common/storage-premium-storage#scalability-and-performance-targets) and [this article](https://docs.microsoft.com/azure/storage/common/storage-scalability-targets#unmanaged-virtual-machine-disks).<br>
