<properties
	pageTitle="RCA for a Customer Initiated VM reboot"
	description="RCA for a Customer Initiated VM reboot"
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
	articleId="4401eb4d-f7a8-491d-8a5b-ff781345bccb"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for a Customer Initiated VM reboot
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC). This expected occurrence was caused by an user initiated reboot action.
The reboot was triggered by an authorized user or process via either Azure Portal or Azure Resource Manager interfaces. As a result, your VM was rebooted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future.

<!--/issueDescription-->

## **Recommended Documents**
  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)