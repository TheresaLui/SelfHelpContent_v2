<properties
	pageTitle="VMA RCA"
	description="RCA - Customer Initiated - VM reboot"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_2CCE8302-7414-4828-B536-50A731ADB90E"
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
 
We identified that your VM became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This expected occurrence was caused by a **user initiated reboot action**.
<!--/issueDescription-->

The reboot was triggered by an authorized user or process via either Azure Portal or Azure Resource Manager interfaces. As a result, your VM was rebooted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.     

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>
To learn more about Azure Resource Health, please refer to the following article:<br>
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)