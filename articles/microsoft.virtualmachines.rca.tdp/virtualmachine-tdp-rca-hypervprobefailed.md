<properties
	pageTitle="Deployment Failure RCA"
	description="RCA-hypervprobefailed"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-hypervprobefailed"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed. This problem occurs when a Linux virtual machine does not communicate with the Azure host within a set amount of time. The communication failure occurred in this deployment because of a known issue relating to incompatible hyper-call timing parameters in the Hyper-V drivers found in older Linux kernels. Your virtual machine is most likely running an older Linux kernel.
<!--/issueDescription-->

To understand how to self-mitigate and understand the kernel versions that may be impacted, [please read this article](https://support.microsoft.com/help/4041171).<br>

Microsoft also recommends updating any custom images that may be used in future deployments to avoid this issue.<br>
