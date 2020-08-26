<properties
	pageTitle="VMA RCA"
	description="RCA - Unhealthy Node - Host OS PowerCycle Inconclusive OrganicRecovery"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="NatErns"
	ms.author="naterns"
	displayOrder=""
	articleId="VMA_RCA_UnhealthyNode_Host_OS_PowerCycle_Inconclusive_OrganicRecovery"
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
We identified that your VM **<!--$vmname-->Virtual machine<!--/$vmname-->** became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. TThis unexpected occurrence was caused by an Azure initiated host node reboot action. During these activities RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed.
<!--/issueDescription-->

This unexpected occurrence was caused due to a platform bug that caused the physical server hosting your VM to become temporarily unresponsive. Our core Azure Engineering teams are tracking this incident and are working on a solution for this issue.  Unfortunately, at the moment we do not have an ETA for the fix.  A related fix involving a specific bug involving hyper-v deadlock has been identified and is currently undergoing testing and validation. Additional telemetry and diagnostics are being instrumented and deployed to the platform in the following layers to understand this issue better:

     - Software layer: OS Kernel, Hypervisor
     - Hardware layer:  BIOS, Firmware
     - Azure monitoring and diagnostics layer.

Additionally, Azure team is also investing in an effort to increase resiliency and improve VM availability.  [More information on improving Azure virtual machine resiliency](https://azure.microsoft.com/blog/improving-azure-virtual-machines-resiliency-with-project-tardigrade/)

We apologize for any inconvenience this may have caused to you.

Microsoft Azure Team
<br>

To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set.<br>

## **Recommended Documents**

* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
