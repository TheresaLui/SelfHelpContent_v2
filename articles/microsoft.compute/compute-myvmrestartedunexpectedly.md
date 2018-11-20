<properties
	pageTitle="My VM restarted unexpectedly"
	description="My VM restarted unexpectedly"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32411816,32593740,32628269,32628280,32628287"
	resourceTags="windows, windowsSQL"
	productPesIds="14749,14745"
	cloudEnvironments="public"
/>

# My VM restarted unexpectedly

4 out of 5 customers resolved their restart issue using below steps:

## **Recommended steps**

The common reasons for a VM restarting are: Azure caused (planned or unpanned maintenance or outage), or issues with the OS or application. Use the following steps to find out the reason for a past restart and to mitigate possible future occurrences.<br>

1. Review [Resource Health](data-blade:resourcehealthdetailblade.resourceId.$resourceId) for the impacted VM.<br>
2. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter.subscriptionId.$subscriptionId) for the time period of the restart to determine the reason.<br>

## **Recommended documents**

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>
* [How to view VM reboot logs to identify the cause of reboot](https://azure.microsoft.com/blog/viewing-vm-reboot-logs)<br>
* [Diagnose & recover from boot failures after a restart](https://azure.microsoft.com/blog/boot-diagnostics-for-virtual-machines-v2/)<br>
* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability)<br>
* [Configure availability sets for virtual machines using Resource Manager deployments](https://docs.microsoft.com/azure/virtual-machines/windows/create-availability-set)<br>
* [Understand planned maintenance and how it is communicated for virtual machines in Azure](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)<br>
* [Service Healing - Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)
