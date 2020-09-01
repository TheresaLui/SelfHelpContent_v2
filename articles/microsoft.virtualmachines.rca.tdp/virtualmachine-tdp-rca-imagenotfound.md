<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-imagenotfound"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-imagenotfound"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to the image specified in the deployment not being found.
<!--/issueDescription-->

To self-mitigate, please verify that the image you are trying to deploy is available for your subscription or verify that the publisher has not removed the image. If the publisher has removed the image, please contact the publisher directly. In addition, some offers are only available to certain subscriptions.<br>

We apologize for any inconvenience this may have caused you.<br>
