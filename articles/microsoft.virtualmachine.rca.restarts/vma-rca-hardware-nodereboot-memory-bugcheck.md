<properties
	pageTitle="VMA RCA"
	description="Root Cause Analysis (RCA) - Hardware - Memory"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""	
	articleId="VMA_RCA_Hardware_NodeReboot_Memory_Bugcheck"
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
The Azure monitoring and diagnostics systems identified that your VM **<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. During this time, RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed.
<!--/issueDescription-->

<!--rcaDescription-->
### **Root Cause**
> The host node where the VM was running encountered a **Memory Error**.  
> 

<!--resolutionDetails-->
### **Resolution**
> The physical node has been taken out of service for further diagnostics and repair. The VM was service healed and restored on a healthy node.
> 
<!--/resolutionDetails-->

<!--additionalInfo-->
### **Additional Information**
> The Hardware Engineering team is working on the following long-term fixes to reduce the impact of these errors:
> - Azure is continually working to make improvements to pre-production hardware screening
> - Azure is continually working with manufacturers to identify and prevent failures through improvements in CPU microcode
> - Improvements to CPU failure handling to reduce or avoid impact to customers
> - Improvements to failure prediction telemetry and models
> 
> We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.
> 
<!--/additionalInfo-->
<!--/rcaDescription-->

<!--recommendedActions-->
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
