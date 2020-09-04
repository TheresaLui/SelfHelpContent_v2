<properties
	pageTitle="VMA RCA"
	description="RCA - Hardware NodeReboot - Networking NMAgent"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Hardware_NodeReboot_Networking_NMAgent"
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
We identified that your VM **<!--$vmname--> Virtual machine <!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated host node reboot action**.
<!--/issueDescription-->

Microsoft Azure team has finished investigating the issue with your virtual machine. The physical host node where your VM was running was undergoing a regular maintenance of the networking stack. This impacted connectivity briefly.

Azure periodically performs updates to improve the reliability, performance, and security of the host infrastructure for virtual machines. There is an expected downtime during these updates. We are continuously working on improving the platform and apologize for any inconvenience this may have caused to you.

If the VM experienced downtime or connectivity loss during this update, it is to be expected. There is guidance (for [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events) and [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events) on how to prepare and design for such maintenance.
 
Note that [virtual functions are expected to be revoked during servicing updates](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli?toc=%2Fazure%2Fvirtual-machines%2Flinux%2Ftoc.json#handle-dynamic-binding-and-revocation-of-virtual-function).
 
We are continuously working on improving the platform and apologize for any inconvenience this may have caused to you.
More information: <https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events>
 
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
