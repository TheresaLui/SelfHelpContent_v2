<properties
	pageTitle="RCA for a Customer Initiated VM Shutdown"
	description="RCA for a Customer Initiated VM Shutdown"
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
	articleId="c2b06c2d-cd7f-4a05-bb7f-54ae9d63c644"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for a Customer Initiated VM Shutdown
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC). This expected occurrence was caused by an user initiated shutdown action.
The shutdown was triggered by an authorized user or process via either Azure Portal or Azure Resource Manager interfaces. As a result, your VM was shut down and remained in this state until user action was taken to restart it.

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future.

<!--/issueDescription-->

## **Recommended Documents**
  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)