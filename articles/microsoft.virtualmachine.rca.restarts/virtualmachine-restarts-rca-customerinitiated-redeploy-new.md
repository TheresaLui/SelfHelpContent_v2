<properties
	pageTitle="VMA RCA"
	description="RCA - Customer Initiated - Redeploy"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
ms.author="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_Customer_Initiated_Redeploy"
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
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. This expected occurrence was caused by a **user initiated redeploy action**.
<!--/issueDescription-->

The redeploy action was triggered by an authorized user or process from either the Azure Portal or Azure Resource Manager interfaces. As a result, your VM was moved to a different host node. This caused your VM to get rebooted. RDP connections to the VM, or requests to any other services running inside the VM, could have failed during this time.<br>

## **Recommended Documents**

* [Use Azure redeploy functionality to transfer virtual machines to a new host](https://azure.microsoft.com/updates/use-azure-redeploy-functionality-to-transfer-virtual-machines-to-a-new-host/)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
