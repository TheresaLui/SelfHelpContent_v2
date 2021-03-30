<properties
	pageTitle="VMA RCA"
	description="Root Cause Analysis (RCA) - Software - Bug - Service Healed"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""	
	articleId="VMA_RCA_Software_NodeFault_Bug_ServiceHealed"
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
> The auto-recovery action was triggered by our Azure monitoring systems that detected a failure condition caused by a recently discovered platform bug with the physical node where the virtual machine was hosted. This caused your VM to be rebooted.
> 

<!--resolutionDetails-->
### **Resolution**
> The VMs on this node have been Service Healed onto a healthy node to avoid further impact.  The unhealthy node has been taken out of service for analysis and repair.  Our core engineers are working to minimize such occurrences.
> 
<!--/resolutionDetails-->

<!--additionalInfo-->
### **Additional Information**
> Our core platform engineers are working on a fix for the platform bug that will be deployed to all affected nodes. To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.
> 
<!--/additionalInfo-->
<!--/rcaDescription-->

<!--recommendedActions-->
## **Recommended Steps**
> To check if SLA was violated: 
> * [SLA for Virtual Machines](https://azure.microsoft.com/support/legal/sla/virtual-machines/v1_8)
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
