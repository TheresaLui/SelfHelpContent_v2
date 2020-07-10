<properties
	pageTitle="RCA for E17 events causes by failed IO transactions due to slow backend operations"
	description="RCA for E17 events causes by failed IO transactions due to slow backend operations"
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
	articleId="e9f1016a-0526-4891-ac54-0c65bb659579"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for E17 events causes by failed IO transactions due to slow backend operations
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This unexpected occurrence was caused by an Azure initiated temporary VM shutdown triggered by detection of temporary IO transaction timeouts between the physical host node where your VM was running, and the Azure Storage service where your Virtual Hard Disks (VHDs) reside.
Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage.  If the transactions are too slow or do not complete successfully within 120 seconds (inclusive of retries), connectivity is considered to be lost and temporary VM shutdown is initiated to preserve data integrity and prevent corruption of your VHDs. Once the platform detected that the Storage service connectivity was restored, the VM was automatically restarted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.
To ensure high availability for your application in Azure, it is recommended that you group two or more virtual machines in an Availability Set and use Managed Disks. To learn more about high availability options, please refer to the articles below. 
Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.

To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future  

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)