<properties
	pageTitle="Your virtual machine is stopping and deallocating as requested by an authorized user or process"
	description="Virtual Machine Deallocation Initiated"
	infoBubbleText="Please take a look at the details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	articleId="servicehealthinsights-microsoft.compute-virtualmachines-healthannotation_virtualmachinedeallocationinitiated"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealthinsights"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinedeallocationinitiated"
/>

# Your virtual machine is stopping and deallocating as requested by an authorized user or process

We identified that your VM <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable at <!--$startTime--> startTime <!--/$startTime--> (UTC). This expected occurrence was caused by an user initiated shutdown action.

The shutdown was triggered by an authorized user or process via either Azure Portal or Azure Resource Manager interfaces. As a result, your VM was shut down and remained in this state until user action was taken to restart it. 

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.
To learn more about Azure Resource Health, please refer to the following article:

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)