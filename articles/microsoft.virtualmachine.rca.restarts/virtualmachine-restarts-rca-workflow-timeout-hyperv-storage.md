<properties
	pageTitle="VMA RCA"
	description="RCA - Node Hang - Workflow Timeout - HyperV Storage"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="UnexpectedVMReboot_Node_Hang_Workflow_Timeout_HyperV_Storage"
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

The host node reboot was triggered by our Azure monitoring systems detecting that the physical node was not successfully responding to VM operations. We identified that this was caused due to a hyper-v related platform bug involving local (VM) storage stack. VMs that could be relocated to different, healthy nodes were automatically moved before the host node was rebooted. During these activities RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed.
<br>

Our core platform engineers are currently working on the solution for this issue. To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.
<br>

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.<br>

## **Recommended Documents**

* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
