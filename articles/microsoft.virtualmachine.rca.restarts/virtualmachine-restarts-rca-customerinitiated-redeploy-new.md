<properties
	pageTitle="VMA RCA"
	description="RCA - Customer Initiated - Redeploy"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
ms.authors="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_Customer_Initiated_Redeploy"
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

We identified that your VM became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This expected occurrence was caused by a **user initiated redeploy action**.
<!--/issueDescription-->

The redeploy action was triggered by an authorized user or process from either the Azure Portal or Azure Resource Manager interfaces. As a result, your VM was moved to a different host node. This caused your VM to get rebooted. RDP connections to the VM, or requests to any other services running inside the VM, could have failed during this time.<br>

To learn more about this user initiated redeploy action, see [Use Azure redeploy functionality to transfer virtual machines to a new host](https://azure.microsoft.com/updates/use-azure-redeploy-functionality-to-transfer-virtual-machines-to-a-new-host/).

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>

To learn more about Azure Resource Health, see [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview).
