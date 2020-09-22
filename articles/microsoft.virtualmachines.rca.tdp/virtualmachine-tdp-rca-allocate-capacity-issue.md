<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - allocate-capacity-issue"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-virtualmachine-tdp-rca-allocate-capacity-issue"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to the requested VM size not being available in the region that was requested.
<!--/issueDescription-->

It is important to **highlight this is not a quota issue.** The servers in Azure datacenters are partitioned into clusters. Normally, an allocation request is attempted within a datecenter with no issues, but it's possible that certain constraints from the allocation request force the Azure platform to attempt the request in a specific set of clusters. Due to the natural fluctuation of capacity within a datacenter, it was not possible to meet the constraints defined at the time the deployment was initiated.<br>

To learn more about allocation failures:<br>

* [Troubleshoot allocation failures for Windows](https://docs.microsoft.com/azure/virtual-machines/windows/allocation-failure)<br>
* [Troubleshoot allocation failures for Linux](https://docs.microsoft.com/azure/virtual-machines/linux/allocation-failure)

To learn more about resizing:<br>

* [Resizing virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines)

To learn more about sizes supported in each region:<br>

* Products available by region, [follow these instructions](https://azure.microsoft.com/regions/services/)

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>
