<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - virtualmachine-tdp-rca-host-node-switched-to-disk-configuration"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-virtualmachine-tdp-rca-host-node-switched-to-disk-configuration"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed or may have taken longer than expected due to disk configuration change that was performed on the Host during the provisioning phase, leading to the error OSProvisioningTimedOut.
<!--/issueDescription-->

To work around this issue, validate if the VM was deployed successfully in the portal. In most cases, the deployment will continue and complete successfully unless another issue is encountered.<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce issues due to platform issue.<br>