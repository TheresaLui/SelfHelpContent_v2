<properties
	pageTitle="VMA RCA"
	description="Root Cause Analysis (RCA) - Hardware - Network Failure"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_Hardware_NodeReboot_Networking_NMAgent"
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
> Microsoft Azure team has finished investigating the issue with your virtual machine. The physical host node where your VM was running was undergoing a regular maintenance of the networking stack. This impacted connectivity briefly.
> 

<!--resolutionDetails-->
### **Resolution**
> VM was restored following reboot of the host node. Our core engineers are working on improving the platform to minimize such occurrences.
> 
<!--/resolutionDetails-->

<!--additionalInfo-->
### **Additional Information**
> Azure periodically performs updates to improve the reliability, performance, and security of the host infrastructure for virtual machines. There is an expected downtime during these updates.
> 
<!--/additionalInfo-->
<!--/rcaDescription-->

<!--recommendedActions-->
## **Recommended Steps**
> For guideance on how to prepare and design for such maintenance:
> * [Scheduled Events on Windows VMs](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events)
> * [Scheduled Events on Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events)
> 
> Note that virtual functions are expected to be revoked during servicing updates. 
> For guidenace on how to enable Accelerated Networking: 
> * [Create VM Accelerated Networking](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli?toc=%2Fazure%2Fvirtual-machines%2Flinux%2Ftoc.json#handle-dynamic-binding-and-revocation-of-virtual-function)
>

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
