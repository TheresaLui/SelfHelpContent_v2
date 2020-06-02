<properties
	pageTitle="VMA RCA"
	description="RCA - Node Hang - HyperV Operation timeout"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="UnexpectedVMReboot_Node_Hang_Software_Operation_Timeout_HyperV_Storage"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public, Fairfax"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM **<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated host node reboot action**.
<!--/issueDescription-->

The host node reboot was triggered by our Azure monitoring systems that detected a **rare hyper-v related issue involving the storage stack** on the physical node where the virtual machine was hosted. This caused your VM to get rebooted. RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed during this time.

VMs that could be relocated to different, healthy nodes were automatically moved before the host node was rebooted. During these activities RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed.
<br>

The Hardware Engineering team is working on the following long-term fixes to reduce the impact of these errors:

- Azure is continually working with manufacturers to identify and prevent failures through improvements in  ????
- Improved proactive monitoring providing better preventive maintenance to reduce or avoid impact to customers due to operation timeouts
- Improvements to failure prediction telemetry and quality improvements to the ????
<br>

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.<br>

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
