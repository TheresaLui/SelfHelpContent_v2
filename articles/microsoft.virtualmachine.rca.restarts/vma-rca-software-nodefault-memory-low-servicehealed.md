<properties
	pageTitle="VMA RCA"
	description="Root Cause Analysis (RCA) - Software - Low Resources - Service Healed"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""	
	articleId="VMA_RCA_Software_NodeFault_Memory_Low_ServiceHealed"
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
The Azure monitoring and diagnostics systems identified that your VM **<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. During this time, RDP and SSH connections to the VM, or requests to any other services running inside the VM, may have failed.
<!--/issueDescription-->

<!--rcaDescription-->
### **Root Cause**
> This unexpected occurrence was caused due to a platform issue where resources on the physical node were exhausted. Our engineering teams have identified the two main root causes:
> * Memory leaks in a few OS and Azure components
> * A general overall increase in resource usage across various Azure and OS components.
> 

<!--resolutionDetails-->
### **Resolution**
> The VMs on this node have been Service Healed onto a healthy node to avoid further impact.  The unhealthy node has been taken out of service for analysis and repair.  Our core engineers are working to minimize such occurrences.
> 
> The following platform fixes are in process:
> * A host OS update that resolves the known memory leaks is currently in deployment. However, a few nodes must be restarted to recover the resources due to the nature of the leak.  We are monitoring impacted nodes and are gradually recovering these nodes to full capacity.
> * Enhancements and features of various Azure components has resulted in an overall increase in general resource usage, which required updates and refinement of the analytics of resources to be used by VMs and host OS. Additionally, a change to influence the placement the VM on a physical node with more appropriate resources is also being evaluated. These revisions for smooth host VM operations are currently being tested and will be deployed across the fleet.
> 
<!--/resolutionDetails-->

<!--additionalInfo-->
### **Additional Information**
> We are monitoring impacted nodes and have marked them for service so that they can be recovered to full capacity.
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
