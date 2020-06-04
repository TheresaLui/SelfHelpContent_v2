<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - disk wrong type - floppy-disk-read-error"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-floppy-disk-read-error"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed. This problem occurs when the Linux kernel doesn't have drivers for an attached floppy drive installed causing provisioning to time-out.
<!--/issueDescription-->

To self-mitigate this issue, upload a new version of the image without attaching a floppy drive, then redeploy using this new image.<br>
