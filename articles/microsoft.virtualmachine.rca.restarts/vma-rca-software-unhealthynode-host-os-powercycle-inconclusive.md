<properties
	pageTitle="VMA RCA"
	description="RCA - Software Unhealthy Node - Host OS PowerCycle Inconclusive"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Software_UnhealthyNode_Host_OS_PowerCycle_Inconclusive"
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
We identified that your VM **<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by an Azure initiated host node reboot action. During these activities RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed.
<!--/issueDescription-->

This unexpected occurrence was caused by a platform initiated reboot when it was detected that the server hosting your VM had become unresponsive. Our core Azure Engineering teams are tracking this incident and are working on a solution for this issue.  Unfortunately, at the moment we do not have an ETA for the fix.  A related fix involving a specific bug involving hyper-v deadlock has been identified and is currently undergoing testing and validation. Additional telemetry and diagnostics are being instrumented and deployed to the platform in the following layers to understand this issue better:

     - Software layer: OS Kernel, Hypervisor
     - Hardware layer:  BIOS, Firmware
     - Azure monitoring and diagnostics layer

Additionally, Azure team is also investing in an effort to increase resiliency and improve VM availability.  [More information on improving Azure virtual machine resiliency](https://azure.microsoft.com/blog/improving-azure-virtual-machines-resiliency-with-project-tardigrade/)

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
