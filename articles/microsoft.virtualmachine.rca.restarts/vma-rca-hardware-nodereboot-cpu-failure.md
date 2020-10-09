<properties
	pageTitle="VMA RCA"
	description="RCA - Hardware NodeReboot - CPU Failure"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""	
	articleId="VMA_RCA_Hardware_NodeReboot_CPU_Failure"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds=""
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

## VM Availability Event
<!--issueDescription-->
The Azure monitoring and diagnostics systems identified that your VM **<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. 
<!--/issueDescription-->

<!--rcaDescription-->
### Issue Description
This unexpected occurrence was caused by an **Azure initiated host node reboot action** as the result of a detected **hardware issue** due to **CPU errors** on the physical node where the VM was hosted. RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed during this time.

<!--resolutionDetails-->
### Resolution
VM Services were restored following reboot.
<!--/resolutionDetails-->

<!--nextSteps-->
### Next Steps
The Hardware Engineering team is working on the following long-term fixes to reduce the impact of these errors:

- Azure is continually working to make improvements to pre-production hardware screening
- Azure is continually working with manufacturers to identify and prevent failures through improvements in CPU microcode
- Improvements to CPU failure handling to reduce or avoid impact to customers
- Improvements to failure prediction telemetry and models

We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.
<!-/nextSteps-->
<!--/rcaDescription-->

<!--recommendedActions-->
## **Recommended Documents**

**Learn More About:**
* [Maintenance and updates for virtual machines in Azure ](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates)
* [Auto-recovery of Virtual Machines ](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)
* [Configure availability of virtual machines ](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)
* [Managed Disks Overview ](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future ](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
<!--/recommendedActions-->

<!--salutation-->
We apologize for any inconvenience this may have caused you. 

Microsoft Azure Team
<!--/salutation-->
