<properties
	pageTitle="My VM restarted unexpectedly"
	description="My VM restarted unexpectedly "
	service="microsoft.classiccompute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder="31"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="linux,redhat,ubuntu"
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="classiccompute-myvmrestartedunexpectedly-linux-mooncake"
	ownershipId="Compute_VirtualMachines"
/>

# My VM restarted unexpectedly

4 out of 5 customers resolved their VM restart issue using the steps below.

## **Recommended Steps**

The most common reasons for a VM restarting are Azure caused (planned/unplanned maintenance or outage), or issues with the OS or application. Use the following steps to find out the reason for a past restart and to mitigate possible future occurrences:

1. Review [Resource Health](data-blade:Microsoft_Azure_Health.resourcehealthdetailblade.resourceId.$resourceId) for the impacted VM to understand the RCA
2. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter.subscriptionId.$subscriptionId) for the time period of the restart to determine the reason

## **Recommended Documents**

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.azure.cn/service-health/resource-health-overview)
* [How to view VM reboot logs to identify the cause of reboot](https://azure.microsoft.com/blog/viewing-vm-reboot-logs)
* [Diagnose & recover from boot failures after a restart](https://azure.microsoft.com/blog/boot-diagnostics-for-virtual-machines-v2/)
* [Manage the availability of virtual machines](https://docs.azure.cn/virtual-machines/linux/manage-availability)
* [Configure availability sets for virtual machines with Azure CLI](https://docs.azure.cn/virtual-machines/linux/tutorial-availability-sets)
* [Understand planned maintenance for virtual machines in Azure](https://docs.azure.cn/virtual-machines/linux/maintenance-and-updates)
* [Service Healing - Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)
* [Use Azure redeploy functionality to transfer virtual machines to a new Azure node](https://docs.azure.cn/virtual-machines/troubleshooting/redeploy-to-new-node-linux)
