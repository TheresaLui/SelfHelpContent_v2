<properties
	pageTitle="Your virtual machine is stopping as requested by an authorized user or by a process running inside the virtual machine"
	description="Virtual Machine Stopped Internally"
	infoBubbleText="Please take a look at the details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	articleId="servicehealth-microsoft.compute-virtualmachines-healthannotation_virtualmachinestoppedinternally"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealth"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinestoppedinternally"
/>

# Your virtual machine is stopping as requested by an authorized user or by a process running inside the virtual machine

We identified that your VM <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable at <!--$startTime--> startTime <!--/$startTime--> (UTC). This expected occurrence was caused by a user initiated shutdown action.

The shutdown was triggered by an authorized user or process from within the Virtual Machine. As a result, your VM was shut down and remained in this state until user action was taken to restart it. 
 
Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.
To learn more about Azure Resource Health, please refer to the following article:

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)