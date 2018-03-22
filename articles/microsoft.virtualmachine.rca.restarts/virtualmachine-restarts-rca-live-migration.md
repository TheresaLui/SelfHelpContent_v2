<properties
	pageTitle="VMA RCA"
	description="RCA - Live Migration"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="JoZender"
	displayOrder=""
	articleId="UnexpectedVMReboot_Live_Migration"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
## **VM Availability incident diagnostic information for <!--$vmname-->Virtual machine<!--/$vmname-->:** ##

We identified that your VM became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This unexpected occurrence was caused by an **Azure initiated Live Migration operation**.
<!--/issueDescription-->

This caused your VM to be unavailable for about 10 seconds. RDP and SSH connections to the VM, or requests to any other services running inside the VM may have failed during this time.<br>
To learn more about our memory-preserving operations, please refer to the following article:<br>
* [Planned maintenance for virtual machines in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-planned-maintenance/)<br>

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.<br>
To learn more about high availability options, please refer to the following articles:<br>
* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)<br>

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>
To learn more about Azure Resource Health, please refer to the following article:<br>
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.
