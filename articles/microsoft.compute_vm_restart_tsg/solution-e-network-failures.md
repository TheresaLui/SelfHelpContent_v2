<properties
	pageTitle="RCA for E17 events causes by failed IO transactions due to Networking failures"
	description="RCA for E17 events causes by failed IO transactions due to Networking failures"
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
	articleId="190ab77b-56e6-46ce-bcd8-49afe35cd116"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for E17 events causes by failed IO transactions due to Networking failures
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This unexpected occurrence was caused by an Azure initiated temporary VM shutdown
The temporary VM shutdown was triggered by our Azure monitoring systems detecting networking issues between the physical host node where your VM was running, and the Azure Storage services where your VHDs reside. As designed, this action was taken to preserve data integrity of your VM. Once the node detected that conditions had improved, the VM was restarted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.
To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.
To learn more about high availability options, please refer to the articles below.

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.

To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future  

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
