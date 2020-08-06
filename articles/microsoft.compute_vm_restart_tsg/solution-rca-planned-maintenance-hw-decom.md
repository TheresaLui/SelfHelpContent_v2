<properties
	pageTitle="RCA for Planned Maintenance due to Hardware Decommissioning"
	description="RCA for Planned Maintenance due to Hardware Decommissioning"
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
	articleId="5d506714-dea9-4bcd-a3b9-e50018e5ecb4"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for Planned Maintenance due to Hardware Decommissioning
<!--issueDescription-->

We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This expected occurrence was caused by an Azure initiated planned maintenance action for migrating to new hardware.

This planned maintenance has been communicated by Azure to the Azure Subscription owners and co-owners via email including a list of all affected Virtual Machines in your subscription ... insert link to communication. This planned maintenance caused a reboot of your Virtual Machine as it was migrated to the new hardware.

Learn More about planned maintenance:

For more about planned maintenance on Azure, please refer to Planned maintenance for virtual machines in Azure link below. 

For more information on update domains for Virtual Machines, please refer to Manage VM Availability link below.  

For more information on pending reboot on IaaS Virtual Machine, please refer to In-VM Notification Service link below.  

Maintenance is scheduled to only impact one region at a single time in each regional pair. This enables you to deploy VMs across those regions to reduce the impact of the maintenance. All reboots associated with planned maintenance can be viewed in you virtual machine’s reboot logs.  

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.   To learn more about high availability options, please refer to the articles below. 

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future.

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**
 
* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
* [Planned maintenance for virtual machines in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-planned-maintenance/)
* [Manage VM Availability](https://aka.ms/)
* [In-VM Notification Service](https://aka.ms/)
* [Maintenance is scheduled to only impact one region at a single time in each regional pai]()
* [Virtual machine’s reboot logs]()
