<properties
	pageTitle="Deployment Failure RCA"
	description="RCA-hypervprobefailed"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-kernelpanic"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed and the platform detected that the OS experienced a kernel panic during provisioning. One common cause is that the image has an older Linux kernel installed. Your virtual machine is most likely running an older Linux kernel or drivers.
<!--/issueDescription-->

We recommend that you update any custom images that may be used in future deployments to avoid this issue. If this is a Marketplace image, we recommend reaching out to the publisher directly.<br>

For additional information, please read these additional documents:<br>

* To understand the minimum kernel versions required for a Linux VM in Azure, [please read this article](https://support.microsoft.com/help/4041171).<br>
* To manually fix non-boot issues related to kernel panics, follow the directions in [this article](https://blogs.msdn.microsoft.com/linuxonazure/2016/10/09/linux-recovery-manually-fixing-non-boot-issues-related-to-kernel-problems/).<br>


