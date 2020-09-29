<properties
	pageTitle="RCA for Node Fault due to defrag maintenance triggering redeployment"
	description="RCA for Node Fault due to defrag maintenance triggering redeployment"
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
	articleId="efa5fae9-5d72-4447-883f-2dd5f405a826"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RCA for Node Fault due to defrag maintenance triggering redeployment
<!--issueDescription-->
We identified that your VM Virtual machine became unavailable at StartTime (UTC) and availability was restored at EndTime (UTC). This unexpected occurrence was caused by an Azure initiated unplanned hardware maintenance action.
The unplanned maintenance action was required in order to ensure the overall health of the Azure Platform. As a result, your VM was automatically moved to a different and healthy physical node to avoid further impact. This caused your VM to get rebooted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.

To learn more about our automated recovery action, please read the articles below. 

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.   To learn more about high availability options, please refer to the articles below.

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal. To learn more about Azure Resource Health, please refer to the Understand and use Resource Health Center to troubleshoot this scenario in the future.

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

<!--/issueDescription-->

## **Recommended Documents**

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)  
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)  
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)
* [Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)