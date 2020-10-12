<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - disks-and-snapshots-cannot-be-resized-down"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-disks-and-snapshots-cannot-be-resized-down"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the disk size specified in the deployment will result in a smaller size than the original size of the VHD.
<!--/issueDescription-->

To work around this issue, please deploy a disk size that is equal or larger than the original size of the disk being deployed.
