<properties
	pageTitle="RCA for Hardware Decommissioning Maintenance"
	description="RCA for Hardware Decommissioning Maintenance"
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
	articleId="a18e6099-2c10-44e9-92ca-56c40c858ce1"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for Hardware Decommissioning Maintenance
<!--issueDescription-->

We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This expected occurrence was caused by an Azure initiated maintenance action.
Azure had previously notified impacted customer about this maintenance. As part of this operation your VM experienced a reboot as it was migrated to newer hardware. RDP and SSH connections to the VM, or requests to any other services running inside the VM may have failed during this time.

To learn more about planned maintenance on Azure, please refer to the following articles below. 

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set. To learn more about high availability options, please refer to the articles below. 

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future. 

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**
 
* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
* [Planned maintenance for virtual machines in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-planned-maintenance/)

