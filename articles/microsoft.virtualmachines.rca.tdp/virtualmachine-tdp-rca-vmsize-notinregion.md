<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-vmsize-notinregion"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-vmsize-notinregion"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of a restriction on the SKU that you are trying to deploy. This resulted in the error:

* There are currently not enough cores of the VM Size Family you requested in this region.
<!--/issueDescription-->

As we expand our Azure infrastructure, we deploy hardware that is not merely 'more of the same'. Instead, our expansion is comprised of newer-generation hardware designed to support the latest virtual machine types. In addition to growing our available infrastructure in each region, this will ultimately provide our customers and partners with higher performing, more versatile, more cost-effective public cloud solutions. Unfortunately the original 'version 1' A, D and DS series VMs do not run on our latest generation infrastructure, so a small number of customers have occasionally seen deployment issues for these legacy SKUs. **To avoid this**, we are encouraging customers using Av1, Dv1 or DSv1 series virtual machines to consider moving to the newer Av2, Dv2, or DSv2 VMs, or better still, consider moving to the newest Dv3 or Ev3 VMs as these are optimized for the latest hardware and will enable customers to take advantage of better price.<br>

To learn more about resizing:<br>

* [Resizing virtual machines](https://azure.microsoft.com/blog/resize-virtual-machines)

To learn more about sizes supported in each region:<br>

* Check the Products available by region [here](https://azure.microsoft.com/regions/services/)

To learn more about allocation failures:<br>

* [Troubleshoot allocation failures for Windows](https://docs.microsoft.com/azure/virtual-machines/windows/allocation-failure)<br>
* [Troubleshoot allocation failures for Linux](https://docs.microsoft.com/azure/virtual-machines/linux/allocation-failure)

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>
