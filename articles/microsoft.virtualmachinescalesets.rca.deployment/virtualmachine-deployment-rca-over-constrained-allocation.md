<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-over-constrained-allocation"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachinescalesets"
	authors="summertgu"
	ms.author="tiag"
	displayOrder=""
	articleId="VMSS_DeploymentFailure_RCA-over_constrained_allocation"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32641079,32641082,32641076,32641075,32641080,32641074,32641076,32641077,32641072,32641073"
	resourceTags=""
	productPesIds="16080"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine scale set **<!--$vmssname-->Virtual machine scale set<!--/$vmssname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to an allocation issue:

* There are currently not enough cores of the VM Size Family you requested in this region.
<!--/issueDescription-->

This is not a quota issue. To self-mitigate, please use a different VM Size Family or a different region.<br>

To learn more about sizes supported in each region:<br>
* Products available by region, [follow these instructions](https://azure.microsoft.com/regions/services/)<br>

To learn more about troubleshooting allocation failures when you create, restart, or resize:<br>
* [Windows troubleshooting](https://docs.microsoft.com/azure/virtual-machines/windows/allocation-failure)<br>
* [Linux troubleshooting](https://docs.microsoft.com/azure/virtual-machines/linux/allocation-failure)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>
