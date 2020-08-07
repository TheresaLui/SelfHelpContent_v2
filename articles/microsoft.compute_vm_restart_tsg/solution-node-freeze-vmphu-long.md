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
	articleId="d6949f49-f7e0-482b-8580-a8c3487b6da9"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Node Freeze due to VMPHU updates
<!--issueDescription-->

We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This unexpected occurrence was caused by an Azure initiated memory-preserving update action.
The memory-preserving update action was performed on the physical node where the virtual machine was hosted. Due to update issues, the deployment was not progressing as fast as expected . The update process succeeded but your VM was unavailable longer than the expected maximum duration of 30 seconds. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.
To learn more about our memory-preserving updates, please refer to the articles below.

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set. To learn more about high availability options, please refer to the articles below.

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future.

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
* [Planned maintenance for virtual machines in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-planned-maintenance/)