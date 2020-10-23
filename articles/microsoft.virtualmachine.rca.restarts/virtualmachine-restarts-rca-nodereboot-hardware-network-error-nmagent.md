<properties
	pageTitle="VMA RCA"
	description="RCA - Hardware Networking NMAgent Error"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="UnexpectedVMReboot_Node_Reboot_Hardware_Networking_Error_NMAgent"
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
<br>

If the VM experienced downtime or connectivity loss during this update, it is to be expected. There is guidance (for [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events) and [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events) on how to prepare and design for such maintenance.
 
Note that [virtual functions are expected to be revoked during servicing updates](https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli?toc=%2Fazure%2Fvirtual-machines%2Flinux%2Ftoc.json#handle-dynamic-binding-and-revocation-of-virtual-function).
 
We are continuously working on improving the platform and apologize for any inconvenience this may have caused to you.
More information: <https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events>
 
[Azure Dedicated Host](https://azure.microsoft.com/blog/introducing-azure-dedicated-host/) may be an option to consider if you would like more stringent control over the updates in the future.
<br>

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.
<br>

## **Recommended Documents**

* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)<br>
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>
