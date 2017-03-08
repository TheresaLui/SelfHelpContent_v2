<properties
	pageTitle="VMA RCA"
	description="RCA - Node Service Heal - Node Crash"
	infoBubbleText="An RCA has been found"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	displayOrder=""
	articleId="UnexpectedVMReboot_33668E95-C74E-42EE-82F6-AFD3ACCC30BD"
	diagnosticScenario="UnexpectedVMReboot"
	selfHelpType="rca"
	supportTopicIds="32411816"
	resourceTags="windows, linux"
	productPesIds="14749"
	cloudEnvironments="public"
/>

#We ran diagnostics on your resource and found an issue

## **Microsoft Azure VM Availability incident diagnostic information for [vmname]<!--($vmname)-->** ##

Microsoft Azure has concluded our investigation of your Virtual Machine (VM) **[vmname]**<!--($vmname)--> in subscription **[SubscriptionId]**<!--($SubscriptionId)-->. We identified that your VM became **unavailable at [StartTime]<!--($StartTime)--> (UTC)** and **availability was restored at [EndTime]<!--($EndTime)--> (UTC)**. This **unexpected occurrence** was **caused by an Azure initiated temporary VM shutdown**.

The temporary VM shutdown was triggered by our Azure monitoring systems detecting failed IO transaction between the physical host node where your VM was running, and the Azure Storage services where your VHDs reside. As designed, this action was taken to preserve data integrity of your VM. Once the node detected that conditions had improved, the VM was restarted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time.   

*To ensure high availability for your application in Azure it is recommended that you group two or more virtual machines in an availability set. This configuration ensures an increased level of protection and provides redundancy during either a planned or unplanned maintenance events. More information on managing and configuring availability of virtual machine can be found in the following articles:*

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)

Microsoft Azure also provides access to resource health information in the Azure Portal via Azure Resource Health, a service that exposes the health of individual Azure resources and provides actionable guidance to troubleshoot problems. To learn more about Azure Resource Health, please refer to the following article: [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

We apologize for any inconvenience this may have caused to you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.

Regards, Microsoft Azure Team
