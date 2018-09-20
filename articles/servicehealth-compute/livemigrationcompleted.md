<properties
	pageTitle="Your virtual machine is paused because of a memory-preserving Live Migration operation."
	description="Live Migration Completed"
	infoBubbleText="Please take a look at the details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	articleId="servicehealth-microsoft.compute-virtualmachines-healthannotation_livemigrationcompleted"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealth"
	cloudEnvironments="public"
	articleTags="healthannotation_livemigrationcompleted"
/>

# Your virtual machine is paused because of a memory-preserving live migration operation

We identified that your VM <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable at <!--$startTime--> startTime <!--/$startTime--> and availability was restored at <!--$endTime--> EndTime <!--/$endTime--> (UTC).
This unexpected occurrence was caused by an Azure initiated Live Migration operation.

This caused your VM to be unavailable for about 10 seconds. RDP and SSH connections to the VM, or requests to any other services running inside the VM may have failed during this time.
To learn more about our memory-preserving operations, please refer to the following article:

* [Planned maintenance for virtual machines in Azure](https://azure.microsoft.com/documentation/articles/virtual-machines-planned-maintenance/)

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.  
To learn more about high availability options, please refer to the following articles:  

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.
To learn more about Azure Resource Health, please refer to the following article:

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to reduce availability incidents of Virtual Machines.