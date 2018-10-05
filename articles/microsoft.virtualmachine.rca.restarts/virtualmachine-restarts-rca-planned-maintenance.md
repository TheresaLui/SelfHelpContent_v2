<properties
	pageTitle="VMA RCA"
	description="RCA - Planned Maintenance"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_6F7CB386-C0FA-40F6-9E31-0E1F9608D9B4"
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

We identified that your VM became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This expected occurrence was caused by an **Azure initiated planned maintenance action**.
<!--/issueDescription-->

This planned maintenance update required a reboot of your virtual machines to apply the required updates to the infrastructure. The virtual machine was shut down while we patched the infrastructure, and then the virtual machine was restarted.<br>

To learn more about planned maintenance on Azure, please refer to the following article:<br>

* [Planned maintenance for virtual machines in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-planned-maintenance/)

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.<br>

To learn more about high availability options, please refer to the following articles:<br>

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>

To learn more about Azure Resource Health, please refer to the following article:<br>

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.<br>
