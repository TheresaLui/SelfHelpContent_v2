<properties
	pageTitle="Your virtual machine is being redeployed to a different host server as part of a planned maintenance activity. It will be back online after the redeployment completes."
	description="Virtual Machine Redeploy Initiated By Control Plane Due To Planned Maintenance"
	infoBubbleText="Please take a look at the details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	articleId="servicehealth-microsoft.compute-virtualmachines-healthannotation_virtualmachineredeployinitiatedbycontrolplaneduetoplannedmaintenance"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealth"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachineredeployinitiatedbycontrolplaneduetoplannedmaintenance"
/>

# Your virtual machine is being redeployed to a different host server as part of a planned maintenance activity. It will be back online after the redeployment completes.

We identified that your VM <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable at <!--$startTime--> startTime <!--/$startTime--> and availability was restored at <!--$endTime--> EndTime <!--/$endTime--> (UTC).
This expected occurrence was caused by an Azure initiated planned maintenance action.

This planned maintenance update required a reboot of your virtual machines to apply the required updates to the infrastructure. The virtual machine was shut down while we patched the infrastructure, and then the virtual machine was restarted. 
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