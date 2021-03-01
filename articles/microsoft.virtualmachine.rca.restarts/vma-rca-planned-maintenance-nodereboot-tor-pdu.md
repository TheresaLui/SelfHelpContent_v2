<properties
	pageTitle="VMA RCA"
	description="Root Cause Analysis (RCA) - Planned Maintenance - TOR PDU"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Planned_Maintenance_NodeReboot_TOR_PDU"
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
> The VM was impacted due to planned maintenance of the Top of Rack (ToR) or PDU (Power Distribution Unit).  A notification is typically sent to the subscription administrator(s) for such events.
> 

<!--resolutionDetails-->
### **Resolution**
> Upon completion of maintenance, the virtual machine was restored.
> 
<!--/resolutionDetails-->

<!--additionalInfo-->
### **Additional Information**
> Customers can control the distribution of their VMs that are at risk of impact from a single infrastructure failure, like in this case. For more details, please see: https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability. Configure [Service Health Alerts](https://docs.microsoft.com/azure/service-health/alerts-activity-log-service-notifications-portal) to recieve advanced notification of planned updates.
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
> * [Service Health Alerts](https://docs.microsoft.com/azure/service-health/alerts-activity-log-service-notifications-portal)
> * [Scheduled Events](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events)
<!--/recommendedActions-->


<!--salutation-->
We apologize for any inconvenience this may have caused you. 

Microsoft Azure Team
<!--/salutation-->
