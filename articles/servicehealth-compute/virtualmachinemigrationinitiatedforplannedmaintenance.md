<properties
	pageTitle="Your virtual machine is unavailable because it is being redeployed to newer hardware as part of a planned maintenance event"
	description="Virtual Machine Migration Initiated For Planned Maintenance"
	infoBubbleText="Please take a look at the details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	articleId="servicehealthinsights-microsoft.compute-virtualmachines-healthannotation_virtualmachinemigrationinitiatedforplannedmaintenance"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealthinsights"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinemigrationinitiatedforplannedmaintenance"
/>

# Your virtual machine is unavailable because it is being redeployed to newer hardware as part of a planned maintenance event

We identified that your VM <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable at <!--$startTime--> startTime <!--/$startTime--> and availability was restored at <!--$endTime--> EndTime <!--/$endTime--> (UTC).
This expected occurrence was caused by an Azure initiated maintenance action. 

Azure had previously notified impacted customer about this maintenance. As part of this operation your VM experienced a reboot as it was migrated to newer hardware. RDP and SSH connections to the VM, or requests to any other services running inside the VM may have failed during this time.  
 
To learn more about planned maintenance on Azure, please refer to the following article:

* [Planned maintenance for virtual machines in Azure](https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-planned-maintenance/)

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.  
To learn more about high availability options, please refer to the following articles:  

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)
* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.
To learn more about Azure Resource Health, please refer to the following article:

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to reduce the availability incidents of Virtual Machines due to platform issue.