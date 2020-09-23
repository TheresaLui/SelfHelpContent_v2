<properties
	pageTitle="VMA RCA"
	description="RCA - Hardware NodeReboot - Memory Bugcheck"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""	
	articleId="VMA_RCA_Hardware_NodeReboot_Memory_Bugcheck"
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
We identified that your VM **<!--$vmname-->Virtual machine<!--/$vmname-->** experienced downtime at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated host node reboot action**.
<!--/issueDescription-->

The host node reboot was triggered by our Azure monitoring systems that detected a **Memory Error** on the physical node where the virtual machine was hosted. This node has been taken out of service for debugging and your VM has been transferred over to a different node. RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed during this time.

The Hardware Engineering team is working on the following long-term fixes to reduce the impact of these errors:

- Azure is continually working to make improvements to pre-production hardware screening
- Azure is continually working with manufacturers to identify and prevent failures through improvements in CPU microcode
- Improvements to CPU failure handling to reduce or avoid impact to customers
- Improvements to failure prediction telemetry and models

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
