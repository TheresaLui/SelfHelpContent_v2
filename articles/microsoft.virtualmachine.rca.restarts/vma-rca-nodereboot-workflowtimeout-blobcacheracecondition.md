<properties
	pageTitle="VMA RCA"
	description="RCA - Node Reboot - VWorkflow timeout - Blob Cache Race Condition"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_NodeReboot_WorkflowTimeOut_BlobCacheRaceCondition"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds=""
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM **<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by an Azure initiated host node reboot action. During these activities RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed.
<!--/issueDescription-->

We identified the host node where the VM was running was impacted due to a recently discovered platform issue.  The root cause was due to a rare race condition in the Azure storage component during routine cleanup associated with VM deallocation.  Our platform engineers have identified the required fixes for this issue and tracking them with priority to get them deployed.

We apologize for any inconvenience this may have caused to you.

Microsoft Azure Team
<br>

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.<br>

## **Recommended Documents**

* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
