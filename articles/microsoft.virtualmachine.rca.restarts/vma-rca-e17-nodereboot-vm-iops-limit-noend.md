<properties
	pageTitle="VMA RCA"
	description="RCA - E17 NodeReboot - IOPS limit"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""	
	articleId="VMA_RCA_E17_NodeReboot_VM_IOPS_Limit_noend"
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
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> experienced downtime at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated VM shutdown** triggered by detection of **temporary IO transaction timeouts** between the physical host node where your VM was running, and the Azure Storage services where your Virtual Hard Disks (VHDs) reside.
<!--/issueDescription-->

Azure Standard Storage disks have a limit of 500 IOPS for each VHD.  We have documented a few best practices for [Configuring Azure Virtual Machines for Optimal Storage Performance ](http://blogs.msdn.com/b/mast/archive/2014/10/14/configuring-azure-virtual-machines-for-optimal-storage-performance.aspx)<br> 

Depending on the workload, a striped disk or configuring Storage Spaces inside the Guest VM may help mitigate the issue.  You may also want to consider Premium Storage if the issue persists.<br>

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.

Microsoft Azure Term
<br>

## **Recommended Documents**

Learn more about:
* [Maintenance and updates for virtual machines in Azure ](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates)
* [Auto-recovery of Virtual Machines ](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)
* [Configure availability of virtual machines ](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)
* [Managed Disks Overview ](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future ](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
<br>
