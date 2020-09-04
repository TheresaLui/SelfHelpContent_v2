<properties
	pageTitle="VMA RCA"
	description="RCA - Software NodeCrash - Guest OS - Windows"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="naterns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Software_NodeCrash_GuestOS_Windows"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM **<!--$vmname-->Virtual Machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by a crash in the VM’s operating system due to due to internal checks in the virtual machine that caused the deployment to be terminated.
<!--/issueDescription-->

To avoid potential memory and disk data corruption, the guest operating system stops execution when it detects a serious error condition. This condition can occur for many different reasons, including the following:

- A memory address that causes an access violation
- An unexpected exception or trap
- A faulting kernel mode driver

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.

Microsoft Azure Term
<br>

## **Recommended Steps**

Details about the cause of the termination are written to system event logs and possibly other files. More information on stop errors and how to analyze them can be found here:<br>

* [Windows Bugcheck Analysis](https://social.technet.microsoft.com/wiki/contents/articles/6302.windows-bugcheck-analysis.aspx)<br>
* [Bug Check Code Reference](https://docs.microsoft.com/windows-hardware/drivers/debugger/bug-check-code-reference2)

## **Recommended Documents**

| To learn about ... | See the following ... |
| --- | ---|
| Maintenance and updates | [Maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates) | [Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines) |
| Automated recovery action | 
| High availability options (highly recommended) | [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability) |
| Configuring Availability Sets | [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets) |
| Managed Disks | [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview) |
| Resource health and troubleshooting | [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview) |
<br>
