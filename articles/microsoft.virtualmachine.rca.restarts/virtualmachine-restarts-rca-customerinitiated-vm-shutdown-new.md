<properties
	pageTitle="VMA RCA"
	description="RCA - Customer Initiated - VM shutdown"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_Customer_Initiated_Shutdown"
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
We identified that your VM became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)**. This expected occurrence was caused by a **user initiated shutdown action**.
<!--/issueDescription-->

The shutdown was triggered by an authorized user or process from either the Azure Portal or from Azure Resource Manager interfaces. As a result, your VM was shut down and remained in this state until user action was taken to restart it.<br>

To troubleshoot similar issues in the future, you can use [Azure Resource Health](https://docs.microsoft.com/azure/resource-health/resource-health-overview), which provides insights into the current and past health of your resources.
