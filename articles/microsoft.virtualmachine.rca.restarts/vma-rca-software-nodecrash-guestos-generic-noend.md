<properties
	pageTitle="VMA RCA"
	description="RCA - Software NodeCrash - Guest OS - Generic"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="naterns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Software_NodeCrash_GuestOS_Generic_noend"
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
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> experienced downtime at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**. This unexpected occurrence was caused by a crash in the guest operating system of your VM.
<!--/issueDescription-->

To avoid potential memory and disk data corruption, the guest operating system stops execution when it detects a serious error condition. This condition can occur for many different reasons, including the following:

- A memory address that causes an access violation
- An unexpected exception or trap
- A faulting kernel mode driver

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.

Microsoft Azure Term
<br>

## **Recommended Steps**

To investigate the causes of the VM crash, please use the following references that might be helpful:<br>

| Guest OS | Troubleshooting links |
| --- | --- |
| Windows | [Windows Bugcheck Analysis](https://social.technet.microsoft.com/wiki/contents/articles/6302.windows-bugcheck-analysis.aspx)<br>[Bug Check Code Reference](https://docs.microsoft.com/windows-hardware/drivers/debugger/bug-check-code-reference2)|
| Ubuntu | [Kernel crash dump](https://help.ubuntu.com/lts/serverguide/kernel-crash-dump.html)<br>[Ubuntu wiki - Crash Dump Recipe](https://wiki.ubuntu.com/Kernel/CrashdumpRecipe)|
| SUSE | [Troubleshooting Application Crash or Core Dump](https://www.suse.com/support/kb/doc/?id=7004526)|
| RHEL | [Analyzing the core dump](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/deployment_guide/s1-kdump-crash)<br>[How to troubleshoot kernel crashes, hangs, or reboots with kdump on Red Hat Enterprise Linux](https://access.redhat.com/solutions/6038)<br>[Kernel crash dump guide](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/kernel_administration_guide/kernel_crash_dump_guide)|
<br>

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
