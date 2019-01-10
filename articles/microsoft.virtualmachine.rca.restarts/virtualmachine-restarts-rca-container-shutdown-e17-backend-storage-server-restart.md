<properties
	pageTitle="VMA RCA"
	description="RCA - Container shutdown - E17 Backend Storage Server Restart"
	infoBubbleText="Found recent reboot. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	displayOrder=""
	articleId="UnexpectedVMReboot_RCA-Container_shutdown-E17_Backend_Storage_Server_Restart"
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
This unexpected occurrence was caused by an **Azure initiated VM shutdown** triggered by detection of **temporary IO transaction timeouts** between the physical host node where your VM was running, and the Azure Storage service where your Virtual Hard Disks (VHDs) reside. The IO timeouts occurred due to an unexpected processing delay in the Stream layer of the Storage service.
<!--/issueDescription-->

Azure platform continuously monitors reads and writes (IO transactions) from your VMs to Azure Storage.  If transactions are too slow or do not complete successfully within 120 seconds (inclusive of retries), the connectivity is considered to be lost and temporary VM shutdown is initiated to preserve the data integrity and prevent corruption of your VM. Once the platform detected that Storage service connectivity was restored, the VM was automatically restarted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.<br>

The Stream layer of Azure Storage stores the data on disk and is in charge of distributing and replicating the data across many servers within the Storage stamp (Extent Nodes) to keep it durable. The Stream Manager manages data placement across the Extent Nodes in the Storage stamp. Due to unexpected  processing delays at the Stream layer, storage operations took longer than expected to complete. The issue was detected and automatically mitigated by our in-built recovery mechanisms, and VM availability was restored.<br>

For more information on the Stream layer of Azure Storage , please refer to the paper [here](http://sigops.org/sosp/sosp11/current/2011-Cascais/printable/11-calder.pdf).<br>

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.<br>

To learn more about high availability options, please refer to the following articles:<br>

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)<br>
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)<br>
* [Managed Disks Overview](https://docs.microsoft.com/azure/storage/storage-managed-disks-overview)

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.<br>

To learn more about Azure Resource Health, please refer to the following article:<br>

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.<br>
