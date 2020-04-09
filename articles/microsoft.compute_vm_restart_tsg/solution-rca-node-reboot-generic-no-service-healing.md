<properties
	pageTitle="Generic RCA for Node Reboots without service healing"
	description="Generic RCA for Node Reboots without service healing"
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
	articleId="21496fdf-ee0f-4122-92ab-fd7b16734cc9"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Generic RCA for Node Reboots without service healing
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This unexpected occurrence was caused by an Azure initiated host node reboot action.
The host node reboot was triggered by our Azure monitoring systems detecting a potential failure condition with the physical node where the virtual machine was hosted. This caused your VM to get rebooted as well. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set. To learn more about high availability options, please refer to the articles below. 

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future.

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**
 
* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)