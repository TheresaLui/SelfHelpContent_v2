<properties
	pageTitle="RCA for E17 events causes by failed IO transactions due to partition server failure"
	description="RCA for E17 events causes by failed IO transactions due to partition server failure"
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
	articleId="91e65556-53df-440b-a60d-1b65f9e7478f"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for E17 events causes by failed IO transactions due to partition server failure
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC).
This unexpected occurrence was caused by an Azure initiated temporary VM shutdown triggered by detection of temporary IO transaction timeouts between the physical host node where your VM was running, and the Azure Storage service where your Virtual Hard Disks (VHDs) reside. The IO timeouts occurred due to a load balancing operation that took longer than expected.
Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage.  If transactions are too slow or do not complete successfully within 120 seconds inclusive of retries, the connectivity is considered lost and temporary VM shutdown is initiated to preserve data integrity and prevent corruption of your VM. Once the platform detected that the Storage service connectivity was restored, the VM was automatically restarted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.
Azure Storage is a multitenant environment, which means there are multiple storage accounts being served by a single storage cluster.  Azure Storage uses a partitioning system that automatically load balances partitions across multiple servers in the cluster based on traffic. Load balancing identifies when a given partition server is resource constrained and reassigns one or more partition ranges to less utilized partition servers. This operation took a longer time to complete than normally expected. Once the operation completed, the data in the partition became available and VM availability was restored.
For more details on load balancing and partition server failures, refer to this document: Microsoft Azure Storage architecture overview  
For details on how your partition naming convention can be designed to enable optimal load-balancing, please refer to the associated section in the Storage Performance and Scalability checklist.

To ensure high availability for your application in Azure, it is recommended that you group two or more virtual machines in an Availability Set and use Managed Disks. To learn more about high availability options, please refer to the articles below. 

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future  

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
* [Microsoft Azure Storage architecture overview](https://blogs.msdn.microsoft.com/windowsazurestorage/2010/12/30/windows-azure-storage-architecture-overview/)
* [associated section in the Storage Performance and Scalability checklist ](https://docs.microsoft.com/azure/storage/storage-performance-checklist#subheading47)