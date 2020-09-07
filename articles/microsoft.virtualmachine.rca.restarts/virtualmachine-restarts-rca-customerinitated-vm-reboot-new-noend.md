<properties
	pageTitle="Virtual Machine Connectivity Issue: VMA RCA"
	description="Virtual Machine Connectivity Issue: VMA RCA"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_Customer_Initiated_Reboot_noend"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Virtual Machine Connectivity Issue: VMA RCA

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> experienced downtime at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**. This expected occurrence was caused by a **user initiated reboot action**.
<!--/issueDescription-->

The reboot was triggered by an authorized user or process from either the Azure Portal or Azure Resource Manager interfaces. As a result, your VM was rebooted. RDP connections to the VM, or requests to any other services running inside the VM, could have failed during this time.<br>

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>

## **Recommended Documents**

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
* To understand more about the user-initiated reboot, refer to [Understand a system reboot for Azure VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#user-initiated-reboot-or-shutdown-actions)
