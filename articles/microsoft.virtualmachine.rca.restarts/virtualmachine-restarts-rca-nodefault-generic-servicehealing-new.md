<properties
	pageTitle="VMA RCA"
	description="RCA - Node Service Heal - Node Crash"
	infoBubbleText="Found recent reboot. See details on the right."
	service=""
	resource=""
	authors="ScottAzure"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_Service_Healing_Node_Fault_Generic"
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
We identified that your VM <!--$vmname--> Virtual machine <!--/$vmname--> became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated auto-recovery action**.
<!--/issueDescription-->

The host node reboot was triggered by our Azure monitoring systems that detected a **potential failure condition with the node** where the virtual machine was hosted. As a result, your VM was automatically moved to a different and healthy node to avoid further impact. This caused your VM to get rebooted. RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed during this time.
<br>

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.
<br>

## **Recommended Documents**

* [Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)<br>
* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/tutorial-availability-sets)<br>
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>
