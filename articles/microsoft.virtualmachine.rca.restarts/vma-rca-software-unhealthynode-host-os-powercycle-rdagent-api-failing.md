<properties
	pageTitle="VMA RCA"
	description="Root Cause Analysis (RCA) - Software - Unhealthy Node"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Software_UnhealthyNode_Host_OS_PowerCycle_RdAgent_API_failing"
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
> This unexpected occurrence was caused by a platform initiated reboot when it was detected that a critical hosting environment service had become unresponsive.
> 

<!--resolutionDetails-->
### **Resolution**
> VM was restored following reboot of the host node.
> 
<!--/resolutionDetails-->

<!--additionalInfo-->
### **Additional Information**
> Our core Azure Engineering teams are tracking this incident and are working on a solution for this issue.  Additional telemetry and diagnostics are being instrumented and deployed to the platform in the following layers to understand this issue better:
> 
> - Software layer: OS Kernel, Hypervisor
> - Hardware layer:  BIOS, Firmware
> - Azure monitoring and diagnostics layer
> 
> Additionally, Azure team is also investing in an effort to increase resiliency and improve VM availability.  [More information on improving Azure virtual machine resiliency](https://azure.microsoft.com/blog/improving-azure-virtual-machines-resiliency-with-project-tardigrade/)
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
