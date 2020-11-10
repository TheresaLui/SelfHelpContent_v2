<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-over-constrained-allocation"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-over_constrained_allocation"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to an allocation issue:

* There are currently not enough cores of the VM Size Family you requested in this region.
<!--/issueDescription-->

This is not a quota issue. To self-mitigate, please use a different VM Size Family or a different region.<br>

To learn more about sizes supported in each region:<br>
* Products available by region, [follow these instructions](https://azure.microsoft.com/regions/services/)<br>

To learn more about troubleshooting allocation failures when you create, restart, or resize:<br>
* [Windows troubleshooting](https://docs.microsoft.com/azure/virtual-machines/windows/allocation-failure)<br>
* [Linux troubleshooting](https://docs.microsoft.com/azure/virtual-machines/linux/allocation-failure)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>