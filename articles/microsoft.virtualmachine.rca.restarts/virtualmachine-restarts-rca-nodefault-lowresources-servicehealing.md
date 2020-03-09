<properties
	pageTitle="VMA RCA"
	description="RCA - Node Service Heal - Node Crash"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_150D3F99-8691-4A4D-9FB5-1654945023A6"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public, Fairfax"
	ownershipId="Compute_ComputePlatform"
/>
# We ran diagnostics on your resource and found an issue


## **VM Availability incident diagnostic information for <!--$vmname-->Virtual machine<!--/$vmname-->

<!--issueDescription-->
We identified that your VM became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated auto-recovery action**.
<!--/issueDescription-->

The auto-recovery action was triggered by our Azure monitoring systems after detecting that the physical node where the virtual machine was hosted was running low on resources. As a result, your VM was automatically moved to a different and healthy physical node to avoid further impact. This caused your VM to get rebooted. RDP and SSH connections to the VM, or requests to any other services running inside the VM, could have failed during this time.<br>

## **Recommended Steps**

Our core platform engineers identified the backend service issue and are currently working on a fix that will be deployed to all affected nodes.<br>

* To learn more about our automated recovery action, see [Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)
* To ensure an increased level of protection and redundancy for your application in Azure, we recommend that you group two or more virtual machines in an availability set
* To learn more about high availability options, refer to the following articles:<br>

	* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
	* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)

* Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal
* To learn more about Azure Resource Health, see [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

We apologize for any inconvenience this may have caused you. We are continuously working to improve the platform to reduce incidences of virtual machine unavailability.<br>
