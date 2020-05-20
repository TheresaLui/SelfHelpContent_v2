<properties
	pageTitle="RCA for a Customer Initiated in-VM shutdown"
	description="RCA for a Customer Initiated in-VM shutdown"
	service="microsoft.compute"
	resource="Microsoft.Compute/virtualMachines"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="6f59d81e-0778-4055-bc12-e74a2ad7f8fe"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for a Customer Initiated in-VM shutdown
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC). This expected occurrence was caused by an user initiated shutdown action.
The redeploy action was triggered by an authorized user or process via either Azure Portal or Azure Resource Manager interfaces. As a result, your VM was moved to a different host node. This caused your VM to get rebooted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time. To learn more about this user initiated redeploy action, please refer to the articles below. 

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future  

<!--/issueDescription-->

## **Recommended Documents**
  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
* [Use Azure redeploy functionality to transfer virtual machines to a new host ](https://azure.microsoft.com/updates/use-azure-redeploy-functionality-to-transfer-virtual-machines-to-a-new-host/)
