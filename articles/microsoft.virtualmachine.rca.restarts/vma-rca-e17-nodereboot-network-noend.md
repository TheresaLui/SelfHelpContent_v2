<properties
	pageTitle="VMA RCA"
	description="RCA - Container shutdown - E17 Network Packet Drop Failure"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_E17_NodeReboot_Network_noend"
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
We identified that your VM **<!--$vmname--> Virtual machine <!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated temporary VM shutdown**.
<!--/issueDescription-->

The physical node where the virtual machine was hosted experienced a **platform bug involving the NIC firmware and drivers used for the Accelerated Networking**. The bug causes sporadic drops in connectivity resulting in a loss of connectivity to storage accounts. 

Our engineering team is proactively applying a temporary mitigation to all affected nodes and actively rolling out a hotfix. 

We regret that this platform bug had an impact on your VM. The Azure engineering teams are investing in both short and long-term initiatives to prevent such incidents going forward.

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.
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
