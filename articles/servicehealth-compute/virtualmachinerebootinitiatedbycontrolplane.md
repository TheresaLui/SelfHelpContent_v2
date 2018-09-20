<properties
	pageTitle="Your virtual machine is rebooting as requested by an authorized user or process. It will be back online after the reboot completes."
	description="Virtual Machine Reboot Initiated By Control Plane"
	infoBubbleText="Please take a look at the details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	articleId="servicehealth-microsoft.compute-virtualmachines-healthannotation_virtualmachinerebootinitiatedbycontrolplane"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealth"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachinerebootinitiatedbycontrolplane"
/>

# Your virtual machine is rebooting as requested by an authorized user or process. It will be back online after the reboot completes.

We identified that your VM <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable at <!--$startTime--> startTime <!--/$startTime--> (UTC). This expected occurrence was caused by a user initiated reboot action.

The reboot was triggered by an authorized user or process via either Azure Portal or Azure Resource Manager interfaces. As a result, your VM was rebooted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time. 

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.
To learn more about Azure Resource Health, please refer to the following article:

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)