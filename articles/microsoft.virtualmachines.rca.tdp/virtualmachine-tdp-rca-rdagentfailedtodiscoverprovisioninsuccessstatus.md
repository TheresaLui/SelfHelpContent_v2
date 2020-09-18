<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rdagentfailedtodiscoverprovisioninsuccessstatus"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-rdagentfailedtodiscoverprovisioninsuccessstatus"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due an intermittent connectivity issues between the Guest VM and its Host during the provisioning phase, leading to an incomplete Provisioning of the VM and the error OSProvisioningTimedOut.
<!--/issueDescription-->

To work around this issue, please redeploy the virtual machine.<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.<br>
