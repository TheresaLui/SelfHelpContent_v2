<properties
	pageTitle="VMA RCA"
	description="RCA - Guest OS Crash - generic"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_GuestOSCrach_Generic"
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
We identified that your VM **<!--$vmname-->Virtual Machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by a crash in the guest operating system of your VM.
<!--/issueDescription-->

To avoid potential memory and disk data corruption, the guest operating system stops execution when it detects a serious error condition. This condition can occur for many different reasons, including the following:

- A memory address that causes an access violation
- An unexpected exception or trap
- A faulting kernel mode driver<br>

## **Recommended Steps**

To investigate the causes of the VM crash, please use the following references that might be helpful:<br>

| Guest OS | Troubleshooting links |
| --- | --- |
| Windows | [Windows Bugcheck Analysis](https://social.technet.microsoft.com/wiki/contents/articles/6302.windows-bugcheck-analysis.aspx)<br>[Bug Check Code Reference](https://docs.microsoft.com/windows-hardware/drivers/debugger/bug-check-code-reference2)|
| Ubuntu | [Kernel crash dump](https://help.ubuntu.com/lts/serverguide/kernel-crash-dump.html)<br>[Ubuntu wiki - Crash Dump Recipe](https://wiki.ubuntu.com/Kernel/CrashdumpRecipe)|
| SUSE | [Troubleshooting Application Crash or Core Dump](https://www.suse.com/support/kb/doc/?id=7004526)|
| RHEL | [Analyzing the core dump](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/deployment_guide/s1-kdump-crash)<br>[How to troubleshoot kernel crashes, hangs, or reboots with kdump on Red Hat Enterprise Linux](https://access.redhat.com/solutions/6038)<br>[Kernel crash dump guide](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/kernel_administration_guide/kernel_crash_dump_guide)|<br>

### Redundancy and health

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set. To learn more about these high availability options, refer to the following articles:<br>

* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)<br>

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more, see the [Azure resource health overview](https://docs.microsoft.com/azure/resource-health/resource-health-overview).
