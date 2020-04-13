<properties
	pageTitle="VMA RCA"
	description="RCA - Guest OS Crash - RHEL"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_GuestOSCrash_Ubuntu"
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

## **Recommended Steps**

Details about the cause of the termination are written to system event logs and possibly other files. To investigate further, see these articles from Ubuntu:<br>

- [Kernel crash dump](https://help.ubuntu.com/lts/serverguide/kernel-crash-dump.html)
- [Ubuntu wiki - Crash Dump Recipe](https://wiki.ubuntu.com/Kernel/CrashdumpRecipe)<br>

### Redundancy and health

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set. To learn more about these high availability options, refer to the following articles:<br>

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)<br>

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more about Azure Resource Health, see [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview).
