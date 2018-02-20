﻿<properties
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
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed. This problem occurs when there the Linux kernel doesn't have drivers for an attached floppy drive causing provisioning to time-out.
<!--/issueDescription-->

To self-mitigat this issue, do not attach a floppy drive device to an image before you upload the image to Azure, upload a new version of the image, and then redeploy on the newer image.<br>