<properties
	pageTitle="VMA RCA"
	description="Root Cause Analysis (RCA) - Software - Low Resources - Service Healed"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""	
	articleId="VMA_RCA_Software_NodeFault_Memory_Fragmented"
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
The Azure monitoring and diagnostics systems identified that the VM **<!--$vmname-->Virtual machine<!--/$vmname-->** was impacted at  **<!--$StartTime--> StartTime <!--/$StartTime-->**.  During this time RDP or SSH connections to the VM, or other such requests could have failed.
<!--/issueDescription-->

<!--rcaDescription-->
### **Root Cause**
> This rare occurrence was caused due to a rare platform issue where the required memory resources were fragmented on the physical node.
> 

<!--resolutionDetails-->
### **Resolution**
> Our core platform engineers are deploying a solution involving memory partitioning which addresses this rare issue.
> 
<!--/resolutionDetails-->

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
