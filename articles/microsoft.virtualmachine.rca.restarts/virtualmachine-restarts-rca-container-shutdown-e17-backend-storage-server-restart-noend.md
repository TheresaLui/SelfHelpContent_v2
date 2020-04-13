<properties
	pageTitle="VMA RCA"
	description="RCA - Container shutdown - E17 Backend Storage Server Restart"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_RCA-Container_shutdown-E17_Backend_Storage_Server_Restart_noend"
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
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> experienced downtime at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated VM shutdown** triggered by detection of **temporary IO transaction timeouts** between the physical host node where your VM was running, and the Azure Storage service where your Virtual Hard Disks (VHDs) reside. The IO timeouts occurred due to an unexpected processing delay in the stream layer of the storage service.
<!--/issueDescription-->

Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage. If transactions do not complete successfully within 120 seconds (inclusive of retries), the connectivity is considered to be lost and a temporary VM shutdown is initiated to preserve data integrity and prevent corruption of your VM. After the platform detects that the storage service connectivity is restored, the VM is automatically restarted. RDP connections to the VM, or requests to any other services running inside the VM, could have failed during this time.<br>

The stream layer of Azure Storage stores the data on disk and ensures durability by  distributing and replicating the data across several servers within the storage stamp (extent nodes). Due to unexpected processing delays at the stream layer, storage operations took longer than expected to complete. The issue was detected and automatically mitigated by our in-built recovery mechanisms, and VM availability was restored.<br>

For more information on the stream layer of Azure Storage, refer to the paper [here](http://sigops.org/sosp/sosp11/current/2011-Cascais/printable/11-calder.pdf).<br>

## **Recommended Steps**

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)<br>
* [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)<br>

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>

To learn more about Azure Resource Health, see [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview).<br>

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.<br>
