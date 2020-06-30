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
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed or may have taken longer than expected. This was due to a disk configuration change that was performed on the physical host during the provisioning of the VM.
<!--/issueDescription-->

This automated disk configuration change needs to be performed before the VM starts and may take several minutes to complete. It is rare for a VM to land on nodes that require this change as the platform monitors and keeps nodes pre-configured. Our core platform engineers have been made aware of this issue and are currently evaluating performance improvements in this area.<br>

In most cases, the deployment will continue and complete successfully. Please validate if the VM was deployed successfully by navigating to the VM blade in the Portal. If the deployment didn’t complete start a new deployment.<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce issues due to platform issue.<br>
