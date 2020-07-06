<properties
	pageTitle="VMA RCA"
	description="RCA - Hardware Node Fault - Disk Slow IO Staging"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="UnexpectedVMReboot_NodeFault_Hardware_Disk_Slow_IO_Staging_noend"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated auto-recovery action**.
<!--/issueDescription-->

We identified that the host node where the VM was running was experiencing a transient platform issue during routine background operations. The background operations activity exposed a Host OS issue, where heavy I/O to local disk impacted the VM network. On the physical node, local disk errors were observed and the node recovered.<br>

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.<br>

## **Recommended Steps**

* We recommend evaluating and consider resizing the VM to an equivalent [v3 series SKU](https://docs.microsoft.com/azure/virtual-machines/sizes-general#dv3-series-1). V3 series VMs will be placed on newer hardware where this issue is less likely to occur.

## **Recommended Documents**

* [Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)
* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

