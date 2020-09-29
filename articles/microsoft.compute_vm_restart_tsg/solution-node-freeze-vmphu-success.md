<properties
	pageTitle="Node Freeze due to VMPHU updates"
	description="Node Freeze due to VMPHU updates"
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
	articleId="6a2a50a3-aae8-47b6-97da-2bf3786cd32b"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Node Freeze due to VMPHU updates
<!--issueDescription-->

We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This unexpected occurrence was caused by an Azure initiated memory-preserving update action.
The memory-preserving update action was performed on the physical node where the virtual machine was hosted. This caused your VM to be unavailable for less than 30 seconds. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time. To learn more about our memory-preserving updates, please refer to the articles below. 

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set. To learn more about high availability options, please refer to the articles below.

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future.

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
* [Planned maintenance for virtual machines in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-planned-maintenance/)