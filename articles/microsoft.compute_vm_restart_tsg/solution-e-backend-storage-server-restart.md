<properties
	pageTitle="RCA for E17 events causes by failed IO transactions due to backend storage server restart"
	description="RCA for E17 events causes by failed IO transactions due to backend storage server restart"
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
	articleId="742bc2b4-d6d0-4481-912e-27fc8168be7d"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for E17 events causes by failed IO transactions due to backend storage server restart
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC).
This unexpected occurrence was caused by an Azure initiated temporary VM shutdown triggered by detection of temporary IO transaction timeouts between the physical host node where your VM was running, and the Azure Storage service where your Virtual Hard Disks (VHDs) reside. The IO timeouts occurred due to an unexpected processing delay in the Stream layer of the Storage service.
Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage.  If transactions are too slow or do not complete successfully within 120 seconds (inclusive of retries), the connectivity is considered to be lost and temporary VM shutdown is initiated to preserve the data integrity and prevent corruption of your VM. Once the platform detected that Storage service connectivity was restored, the VM was automatically restarted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.
The Stream layer of Azure Storage stores the data on disk and is in charge of distributing and replicating the data across many servers within the Storage stamp (Extent Nodes) to keep it durable. The Stream Manager manages data placement across the Extent Nodes in the Storage stamp. Due to unexpected processing delays at the Stream layer, storage operations took longer than expected to complete. The issue was detected and automatically mitigated by our in-built recovery mechanisms, and VM availability was restored.
For more information on the Stream layer of Azure Storage , please refer to the link below.
To ensure high availability for your application in Azure, it is recommended that you group two or more virtual machines in an Availability Set and use Managed Disks. To learn more about high availability options, please refer to the articles below.

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.

To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future  

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)
*[Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
* [Stream Layer of  Azure Storage](http://sigops.org/sosp/sosp11/current/2011-Cascais/printable/11-calder.pdf)
