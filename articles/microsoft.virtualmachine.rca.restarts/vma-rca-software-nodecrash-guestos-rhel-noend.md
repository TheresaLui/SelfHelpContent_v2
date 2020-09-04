<properties
	pageTitle="VMA RCA"
	description="RCA - Software NodeCrash - Guest OS - RHEL"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="naterns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Software_NodeCrash_GuestOS_RHEL_noend"
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
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> experienced downtime at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**. This unexpected occurrence was caused by a crash in the VM’s operating system due to due to internal checks in the virtual machine that caused the deployment to be terminated.
<!--/issueDescription-->

To avoid potential memory and disk data corruption, the guest operating system stops execution when it detects a serious error condition. This condition can occur for many different reasons, including the following:

- A memory address that causes an access violation
- An unexpected exception or trap
- A faulting kernel mode driver

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.

Microsoft Azure Term
<br>

## **Recommended Steps**

Details about the cause of the termination are written to system event logs and possibly other files. To investigate further, see these articles from Red Hat Customer Portal:<br>

Troubleshooting links:
* [RHEL Analyzing the core dump ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/deployment_guide/s1-kdump-crash)
* [RHEL troubleshooting kernel crashes, hangs, or reboots with kdump ](https://access.redhat.com/solutions/6038)
* [RHEL ernel crash dump guide ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/kernel_administration_guide/kernel_crash_dump_guide)

## **Recommended Documents**

Learn more about:
* [Maintenance and updates for virtual machines in Azure ](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates)
* [Auto-recovery of Virtual Machines ](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)
* [Configure availability of virtual machines ](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)
* [Managed Disks Overview ](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future ](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
<br>
