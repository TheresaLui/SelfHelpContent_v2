<properties
	pageTitle="VMA RCA"
	description="RCA - Container shutdown - E17 Partition Server Failure"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_RCA-Container_shutdown-E17_Partition_Server_Failure"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We identified that your VM <!--$vmname-->Virtual machine<!--/$vmname--> became unavailable at **<!--$StartTime--> StartTime <!--/$StartTime--> (UTC)** and availability was restored at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**.
This unexpected occurrence was caused by an **Azure initiated VM shutdown** triggered by detection of **temporary IO transaction timeouts** between the physical host node where your VM was running, and the Azure Storage services where your Virtual Hard Disks (VHDs) reside. The IO timeouts occurred due to a load balancing operation that took longer than expected.
<!--/issueDescription-->

Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage.  If transactions are too slow or do not complete successfully within 120 seconds inclusive of retries, the connectivity is considered lost and temporary VM shutdown is initiated to preserve data integrity and prevent corruption of your VM. Once the platform detected that the Storage service connectivity was restored, the VM was automatically restarted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.<br>

Azure Storage is a multitenant environment, which means there are multiple storage accounts being served by a single storage cluster.  Azure Storage uses a partitioning system that automatically load balances partitions across multiple servers in the cluster based on traffic. Load balancing identifies when a given partition server is resource constrained and reassigns one or more partition ranges to less utilized partition servers. This operation took a longer time to complete than normally expected.  Once the operation completed, the data in the partition became available and VM availability was restored.<br>

For more details on load balancing and partition server failures, refer to this document: <br>

* [Microsoft Azure Storage architecture overview](https://blogs.msdn.microsoft.com/windowsazurestorage/2010/12/30/windows-azure-storage-architecture-overview/)

For details on how your partition naming convention can be designed to enable optimal load-balancing, please refer to the [associated section in the Storage Performance and Scalability checklist](https://docs.microsoft.com/azure/storage/storage-performance-checklist#subheading47).<br>

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.<br>

To learn more about high availability options, please refer to the following articles:<br>

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)<br>
* [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>

To learn more about Azure Resource Health, please refer to the following article:<br>

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.<br>
