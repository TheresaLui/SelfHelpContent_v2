<properties
	pageTitle="RCA for E17 events causes by failed IO transactions due to backend storage server hardware failure migration"
	description="RCA for E17 events causes by failed IO transactions due to backend storage server hardware failure migration"
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
	articleId="52fa5550-7091-41c4-bcec-4e73bf5857a4"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for E17 events causes by failed IO transactions due to backend storage server hardware failure migration
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This unexpected occurrence was caused by an Azure initiated temporary VM shutdown triggered by detection of temporary IO transaction timeouts between the physical host node where your VM was running, and the Azure Storage service where your Virtual Hard Disks (VHDs) reside. The IO timeouts occurred due to a hardware failure and the time taken to migrate to a different backend storage server.
Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage.  If transactions are too slow or do not complete successfully within 120 seconds (inclusive of retries), the connectivity is considered to be lost and the temporary VM shutdown is initiated to preserve data integrity and prevent corruption of your VM. Once the platform detected that the Storage service connectivity was restored, the VM was automatically restarted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.
The impacted VM had VHDs on a backend storage node which experienced a hardware failure. This failure was automatically detected and storage operations for the VHD were redirected to a healthy backend storage server. The time taken to perform this self-healing operation resulted in a delay in processing of the storage requests and temporary VM unavailability. We are continuously working on improving our self-healing capabilities to minimize and even eliminate impact of any hardware failures in the system.

To ensure high availability for your application in Azure, it is recommended that you group two or more virtual machines in an Availability Set and use Managed Disks. To learn more about high availability options, please refer to the articles below. 

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.To learn more about Azure Resource Health, please refer to the artciles below. 

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
