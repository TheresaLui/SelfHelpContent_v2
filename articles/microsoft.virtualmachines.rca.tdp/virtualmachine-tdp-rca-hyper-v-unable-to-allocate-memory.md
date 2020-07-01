<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-hyper-v-unable-to-allocate-memory"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-hyper-v-unable-to-allocate-memory"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** either took longer to deploy or may have reported a failure during provisioning. This is a result of a temporary memory pressure on the node where the VM was initially placed.
<!--/issueDescription-->

To work around this issue, please redeploy your VM if a failure was encountered.<br>

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to make sure that there are less frequent deployment failures specific to this issue.<br>
