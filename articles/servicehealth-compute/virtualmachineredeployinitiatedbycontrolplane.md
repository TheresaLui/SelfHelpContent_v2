<properties
	pageTitle="Your virtual machine is being redeployed to a different host as requested by an authorized user or process. It will be back online after the redeployment completes."
	description="Virtual Machine Redeploy Initiated By Control Plane"
	infoBubbleText="Please take a look at the details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="jozender"
	articleId="servicehealth-microsoft.compute-virtualmachines-healthannotation_virtualmachineredeployinitiatedbycontrolplane"
	diagnosticScenario="health_diagnostic"
	selfHelpType="servicehealth"
	cloudEnvironments="public"
	articleTags="healthannotation_virtualmachineredeployinitiatedbycontrolplane"
/>

# Your virtual machine is being redeployed to a different host as requested by an authorized user or process. It will be back online after the redeployment completes.

We identified that your VM <!--$resourceName--> resourceName <!--/$resourceName--> became unavailable at <!--$startTime--> startTime <!--/$startTime--> (UTC). This expected occurrence was caused by an user initiated shutdown action.

The redeploy action was triggered by an authorized user or process via either Azure Portal or Azure Resource Manager interfaces. As a result, your VM was moved to a different host node. This caused your VM to get rebooted. RDP connections to the VM, or requests to any other services running inside the VM may have failed during this time. 

To learn more about this user initiated redeploy action, please refer to the following article: 

* [Use Azure redeploy functionality to transfer virtual machines to a new host](https://azure.microsoft.com/en-us/updates/use-azure-redeploy-functionality-to-transfer-virtual-machines-to-a-new-host/)

Microsoft Azure also provides access to resource health and troubleshooting information in the Azure Portal.
To learn more about Azure Resource Health, please refer to the following article:

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)