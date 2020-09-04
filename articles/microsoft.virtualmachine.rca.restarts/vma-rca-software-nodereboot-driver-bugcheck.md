<properties
	pageTitle="VMA RCA"
	description="RCA - Software NodeReboot - Driver Bugcheck"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Software_NodeReboot_Driver_Bugcheck"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds=""
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated host node reboot action**.
<!--/issueDescription-->

The host node reboot action was triggered by our Azure monitoring systems that detected a **driver failure condition** on the physical node where the virtual machine was hosted. This caused your VM to get rebooted. RDP connections to the VM, or requests to any other services running inside the VM, could have failed during this time. Our core platform engineers are tracking this issue currently.  If the node is impacted again within 7 days, the node will be taken out of production.

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.

Microsoft Azure Term
<br>

## **Recommended Documents**

| To learn about ... | See the following ... |
| --- | ---|
| Maintenance and updates | [Maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/maintenance-and-updates) | [Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines) |
| Automated recovery action | 
| High availability options (highly recommended) | [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability) |
| Configuring Availability Sets | [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets) |
| Managed Disks | [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview) |
| Resource health and troubleshooting | [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview) |
<br>
