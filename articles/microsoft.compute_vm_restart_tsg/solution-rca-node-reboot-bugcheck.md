<properties
	pageTitle="RCA for Node Reboots without service healing due to node bugcheck"
	description="RCA for Node Reboots without service healing due to node bugcheck"
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
	articleId="495b35b3-5e6e-44b0-aad4-719249a5de9e"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for Node Reboots without service healing due to node bugcheck
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This unexpected occurrence was caused by an Azure initiated host node reboot action.
The host node reboot action was triggered by our Azure monitoring systems detecting a failure condition due to a recently discovered platform bug with the physical node where the virtual machine was hosted. This caused your VM to get rebooted as well. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time. Our core platform engineers have identified the bug and are currently working on a fix for this issue. Once the solution has been verified and completed testing, it will be deployed to all affected nodes.

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set. To learn more about high availability options, please refer to the articles below. 

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future.

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**
 
* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)