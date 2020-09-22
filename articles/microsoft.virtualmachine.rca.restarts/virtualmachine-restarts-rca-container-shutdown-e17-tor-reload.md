<properties
	pageTitle="VMA RCA"
	description="RCA - Container shutdown - E17 Network failures"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_14a0aa18-5da1-45f1-88dc-c6f0f6a5ff99"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

## **VM Availability incident diagnostic information for <!--$vmname-->Virtual machine<!--/$vmname-->**

<!--issueDescription-->
We identified that your VM became unavailable at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)**, and was restored at **<!--$EndTime-->EndTime<!--/$EndTime--> (UTC)**. During this incident, a top of rack (ToR) network router connecting a single rack of servers reloaded after experiencing a hardware failure. This caused temporary IO transaction timeouts between the physical host node where your VM was running and the Azure Storage services where your Virtual Hard Disks (VHDs) reside, resulting in an **Azure initiated temporary VM shutdown**.
 <!--/issueDescription-->

Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage. If transactions do not complete successfully within 120 seconds (inclusive of retries), the connectivity is considered to be lost and a temporary VM shutdown is initiated. This is done to preserve data integrity and prevent corruption of your VM. After the platform detects that the storage service connectivity is restored, the VM is automatically restarted. RDP connections to the VM, or requests to any other services running inside the VM, could have failed during this time.

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.<br>

To learn more about high availability options, refer to the following articles:<br>

* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)<br>

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>

To learn more about Azure Resource Health, see [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview).<br>

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.<br>
