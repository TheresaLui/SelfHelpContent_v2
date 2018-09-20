<properties
	pageTitle="Your virtual machine isn't available because an unexpected failure on the host server"
	description="Virtual Machine Migration Initiated For Unplanned Maintenance"
	infoBubbleText="Please take a look at the details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	articleId="servicehealth-microsoft.compute-virtualmachines-healthannotation_virtualmachinemigrationinitiatedforunplannedmaintenance"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealth"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinemigrationinitiatedforunplannedmaintenance"
/>

# Your virtual machine isn't available because an unexpected failure on the host server

We identified that your VM <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable at <!--$startTime--> startTime <!--/$startTime--> and availability was restored at <!--$endTime--> EndTime <!--/$endTime--> (UTC).
This unexpected occurrence was caused by an unexpected failure on the host server.

The unplanned hardware maintenance action was required in order to ensure the long term reliability of the physical node where the virtual machine was hosted. As a result, your VM was automatically moved to a different and healthy physical node to avoid further impact. This caused your VM to get rebooted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time. 
To learn more about our automated recovery action, please read the following article:

* [Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)

To ensure an increased level of protection and redundancy for your application in Azure, it is recommended that you group two or more virtual machines in an availability set.  
To learn more about high availability options, please refer to the following articles:

* [Manage the availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-manage-availability)

* [Configure availability of virtual machines](https://azure.microsoft.com/documentation/articles/virtual-machines-how-to-configure-availability)

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.

To learn more about Azure Resource Health, please refer to the following article:

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)

We apologize for any inconvenience this may have caused you. We are continuously working on improving the Azure platform to reduce availability incidents of Virtual Machines.