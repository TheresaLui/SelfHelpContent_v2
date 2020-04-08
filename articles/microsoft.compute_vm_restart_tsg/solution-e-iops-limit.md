<properties
	pageTitle="RCA for E17 events causes by exceeding the 500 IOPS limit on standard disks"
	description="RCA for E17 events causes by exceeding the 500 IOPS limit on standard disks"
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
	articleId="37861ad5-b12d-4cd6-bd13-04efe390c7b2"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for E17 events causes by exceeding the 500 IOPS limit on standard disks
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC).
This unexpected occurrence was caused by an Azure initiated VM shutdown triggered by detection of temporary IO transaction timeouts between the physical host node where your VM was running, and the Azure Storage services where your Virtual Hard Disks (VHDs) reside.
Azure Standard Storage disks have a limit of 500 IOPS for each VHD.  We have documented a few best practices for Configuring Azure Virtual Machines for Optimal Storage Performance  
Depending on the workload, a striped disk or configuring Storage Spaces inside the Guest VM may help mitigate the issue.  You may also want to consider Premium Storage if the issue persists. To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set. To learn more about high availability options, please refer to the articles below. 

[Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.

To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future  

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
