<properties
	pageTitle="VMA RCA"
	description="Root Cause Analysis (RCA) - Software BugCheck - Guest OS"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="naterns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Software_BugCheck_GuestOS"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

## **VM Availability**
<!--issueDescription-->
The Azure monitoring and diagnostics systems identified that your VM **<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. During this time RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed.
<!--/issueDescription-->

<!--rcaDescription-->
### **Root Cause**
> This unexpected occurrence was caused by a crash in the guest operating system of your VM.
> 
> To avoid potential memory and disk data corruption, the guest operating system stops execution when it detects a serious error condition. This condition can occur for many different reasons, including the following:
> 
> - A memory address that causes an access violation
> - An unexpected exception or trap
> - A faulting kernel mode driver
> 

<!--resolutionDetails-->
### **Resolution**
> VM was restored following reboot of the host node.
> 
<!--/resolutionDetails-->
<!--/rcaDescription-->

<!--recommendedActions-->## **Recommended Steps**

> To investigate the causes of the VM crash, please use the following references that might be helpful:
> 
> Troubleshooting links:
> * [Windows Bugcheck Analysis](https://social.technet.microsoft.com/wiki/contents/articles/6302.windows-bugcheck-analysis.aspx)
> * [Bug Check Code Reference](https://docs.microsoft.com/windows-hardware/drivers/debugger/bug-check-code-reference2)
> * [Ubuntu Kernel crash dump](https://help.ubuntu.com/lts/serverguide/kernel-crash-dump.html)
> * [Ubuntu wiki - Crash Dump Recipe](https://wiki.ubuntu.com/Kernel/CrashdumpRecipe)
> * [SUSE Troubleshooting Application Crash or Core Dump](https://www.suse.com/support/kb/doc/?id=7004526)
> * [RHEL Analyzing the core dump](https://access.redhat.com/documentation/red_hat_enterprise_linux/6/html/deployment_guide/s1-kdump-crash)
> * [RHEL troubleshooting kernel crashes, hangs, or reboots with kdump](https://access.redhat.com/solutions/6038)
> * [RHEL ernel crash dump guide](https://access.redhat.com/documentation/red_hat_enterprise_linux/7/html/kernel_administration_guide/kernel_crash_dump_guide)
> 

## **Recommended Documents**

> *Learn more about:*
> * [Maintenance and updates for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates)
> * [Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)
> * [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)
> * [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)
> * [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
> 
<!--/recommendedActions-->


<!--salutation-->
We apologize for any inconvenience this may have caused you. 

Microsoft Azure Team
<!--/salutation-->
