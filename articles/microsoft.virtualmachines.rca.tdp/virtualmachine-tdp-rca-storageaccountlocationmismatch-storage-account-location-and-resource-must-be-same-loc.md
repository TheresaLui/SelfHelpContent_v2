<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-storageaccountlocationmismatch-storage-account-location-and-resource-must-be-same-loc"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-storageaccountlocationmismatch-storage-account-location-and-resource-must-be-same-loc"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to the storage account not being resolved. The storage account location and the compute resource are not in the same region.
<!--/issueDescription-->

To mitigate the issue, please validate the location of the storage account and the compute resource as they must be in the same region.<br>