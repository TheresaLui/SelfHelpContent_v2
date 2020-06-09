<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - allocate-failure"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-virtualmachine-tdp-rca-allocate-failure"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to the requested VM size not being available on the cluster where the availability set is pinned.
<!--/issueDescription-->

It is important to **highlight this is not a quota issue.** The servers in Azure datacenters are partitioned into clusters. Normally, an allocation request is attempted in multiple clusters, but it's possible that certain constraints from the allocation request force the Azure platform to attempt the request in only one cluster. Due to the natural fluctuation of capacity within the cluster, it was not possible to meet the constraints defined for the availability set at the time the deployment was initiated.<br>

To learn more about allocation failures including availability sets:<br>
* [Troubleshoot allocation failures for Windows](https://docs.microsoft.com/azure/virtual-machines/windows/allocation-failure)<br>
* [Troubleshoot allocation failures for Linux](https://docs.microsoft.com/azure/virtual-machines/linux/allocation-failure)<br>

To learn more about resizing:<br>
* [Resizing virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines)<br>

To learn more about sizes supported in each region:<br>
* Products available by region, [follow these instructions](https://azure.microsoft.com/regions/services/)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>
