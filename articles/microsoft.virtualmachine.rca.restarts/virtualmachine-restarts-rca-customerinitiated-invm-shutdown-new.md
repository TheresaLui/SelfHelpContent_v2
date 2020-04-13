<properties
	pageTitle="VMA RCA"
	description="RCA - Customer Initiated - in-VM shutdown"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_Customer_Initiated_in-VM_shutdown"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**. This expected occurrence was caused by a **user initiated shutdown action**.
<!--/issueDescription-->

The shutdown was triggered by an authorized user or process from within the Virtual Machine. As a result, your VM was shut down and remained in this state until user action was taken to restart it.<br>

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>

## **Recommended Documents**

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
