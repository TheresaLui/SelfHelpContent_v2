<properties
	pageTitle="VMA RCA"
	description="RCA - Container shutdown - E17 Slow Backend Operation"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_RCA-Container_shutdown-E17_Slow_Backend_Operation_noend"
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
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> experienced downtime at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated temporary VM shutdown** triggered by detection of **temporary IO transaction timeouts** between the physical host node where your VM was running, and the Azure Storage services where your Virtual Hard Disks (VHDs) reside.
<!--/issueDescription-->

Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage. If transactions do not complete successfully within 120 seconds (inclusive of retries), the connectivity is considered to be lost and a temporary VM shutdown is initiated to preserve data integrity and prevent corruption of your VM. After the platform detects that the storage service connectivity is restored, the VM is automatically restarted. RDP connections to the VM, or requests to any other services running inside the VM, could have failed during this time.<br>

## **Recommended Steps**

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.

## **Recommended Documents**

* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)<br>
* [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>

To learn more about Azure Resource Health, see [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview).<br>

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.<br>
