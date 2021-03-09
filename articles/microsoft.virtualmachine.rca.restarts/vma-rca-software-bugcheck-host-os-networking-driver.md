<properties
	pageTitle="VMA RCA"
	description="Root Cause Analysis (RCA) - Software BugCheck- Host OS Networking Driver"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Software_BugCheck_Host_OS_Networking_Driver"
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
> We identified that the physical host node where the VM was running experienced a rare unexpected bug check in a core OS networking driver involving driver kernel stack space usage that resulted in the VM restarting.
> 

<!--resolutionDetails-->
### **Resolution**
> The VMs on this node have been Service Healed onto a healthy node to avoid further impact.  The unhealthy node has been taken out of service for repair. Our core engineers are working to minimize such occurrences.
> 
> Our core networking engineers have already identified the issue and are deploying an OS update following safe deployment practices. We have verified that the VM is running on a node where the OS has already been updated, and is not expected to be impacted again. The update is expected to complete across the entire fleet in the next few weeks. 
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
