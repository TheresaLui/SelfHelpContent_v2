<properties
	pageTitle="VMA RCA"
	description="Root Cause Analysis (RCA) - IO Timeout - Storage Migration"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""	
	articleId="VMA_RCA_IO_Timeout_NodeReboot_XStore_Migration_e17"
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
> This unexpected occurrence was caused by an Azure initiated VM shutdown triggered by the detection of temporary IO transaction timeouts between the physical host node where your VM was running, and the Azure Storage service where your Virtual Hard Disks (VHDs) reside. The IO timeouts occurred due to a hardware failure and the time taken to migrate to a different backend storage server.
> 
> Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage. If transactions do not complete successfully within 120 seconds (inclusive of retries), the connectivity is considered to be lost and a temporary VM shutdown is initiated to preserve data integrity and prevent corruption of your VM. After the platform detects that the storage service connectivity is restored, the VM is automatically restarted.
> 


<!--resolutionDetails-->
### **Resolution**
> The impacted VM had VHDs on a backend storage node that experienced a hardware failure. This failure was automatically detected and storage operations for the VHD were redirected to a healthy backend storage server. The time taken to perform this self-healing operation resulted in a delay in processing of the storage requests and temporary VM unavailability. We are continuously working on improving our self-healing capabilities to minimize and even eliminate impact of any hardware failures in the system.
> 
<!--/resolutionDetails-->

<!--additionalInfo-->
### **Additional Information**
> For general information on storage architecture and for more details on the particular reason of the connectivity loss, refer to the Partition Server Failure section in this document:
> 
> * [Microsoft Azure Storage architecture overview](https://blogs.msdn.microsoft.com/windowsazurestorage/2010/12/30/windows-azure-storage-architecture-overview/)
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
