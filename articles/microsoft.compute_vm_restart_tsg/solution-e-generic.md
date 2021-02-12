<properties
	pageTitle="Generic RCA for E17 events that cause a temporary Container shutdown"
	description="Generic RCA for E17 events that cause a temporary Container shutdown"
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
	articleId="fea7b1a3-4476-4ffe-9329-1b4037873112"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Generic RCA for E17 events that cause a temporary Container shutdown
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This unexpected occurrence was caused by an Azure initiated VM shutdown triggered by detection of temporary IO transaction timeouts between the physical host node where your VM was running, and the Azure Storage services where your Virtual Hard Disks (VHDs) reside.
Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage.  If transactions are too slow or do not complete successfully within 120 seconds (inclusive of retries), connectivity is considered to be lost and the temporary VM shutdown is initiated to preserve the data integrity and prevent corruption of your VM. Once the platform detected that Storage service connectivity was restored, the VM was automatically restarted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.
To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.
To learn more about high availability options, please refer to the articles below.

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.

To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future  

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

