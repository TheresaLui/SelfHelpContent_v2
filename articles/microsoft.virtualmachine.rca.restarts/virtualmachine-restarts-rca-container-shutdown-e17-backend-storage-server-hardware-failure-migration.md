<properties
	pageTitle="VMA RCA"
	description="RCA - Container shutdown - E17 Backend Storage Server Hardware Failure_Migration"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_RCA-Container_shutdown-E17_Backend_Storage_Server_Hardware_Failure_Migration"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**.
This unexpected occurrence was caused by an **Azure initiated VM shutdown** triggered by detection of **temporary IO transaction timeouts** between the physical host node where your VM was running, and the Azure Storage service where your Virtual Hard Disks (VHDs) reside. The IO timeouts occurred due to a hardware failure and the time taken to migrate to a different backend storage server.
<!--/issueDescription-->

Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage. If transactions do not complete successfully within 120 seconds (inclusive of retries), the connectivity is considered to be lost and a temporary VM shutdown is initiated to preserve data integrity and prevent corruption of your VM. After the platform detects that the storage service connectivity is restored, the VM is automatically restarted. RDP connections to the VM, or requests to any other services running inside the VM, could have failed during this time.<br>

The impacted VM had VHDs on a backend storage node that experienced a hardware failure. This failure was automatically detected and storage operations for the VHD were redirected to a healthy backend storage server. The time taken to perform this self-healing operation resulted in a delay in processing of the storage requests and temporary VM unavailability. We are continuously working on improving our self-healing capabilities to minimize and even eliminate impact of any hardware failures in the system.<br>

For general information on storage architecture and for more details on the particular reason of the connectivity loss, refer to the Partition Server Failure section in this document:<br>

* [Microsoft Azure Storage architecture overview](https://blogs.msdn.microsoft.com/windowsazurestorage/2010/12/30/windows-azure-storage-architecture-overview/)<br>

To ensure high availability for your application in Azure, we recommend that you group two or more virtual machines in an Availability Set and use Managed Disks.<br>

To learn more about high availability options, refer to the following articles:<br>

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)<br>
* [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)<br>

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>

To learn more about Azure Resource Health, see [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview).<br>

We apologize for any inconvenience this may have caused you. We are continuously working to reduce the number of availability incidents of Virtual Machines caused by platform issues.<br>