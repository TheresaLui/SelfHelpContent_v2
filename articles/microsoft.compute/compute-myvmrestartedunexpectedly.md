<properties
	pageTitle="My VM restarted unexpectedly"
	description="My VM restarted unexpectedly"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder="25"
	selfHelpType="resource"
	supportTopicIds="32593740,32628269,32628280,32628287"
	resourceTags="windows, windowsSQL"
	productPesIds="14749,14745"
	cloudEnvironments="public"
	articleId="64c0a2f3-0fe4-4eed-a2d2-3218f58cde19"
/>

# My VM restarted unexpectedly

4 out of 5 customers resolved their VM restart issue using the steps below.<br>

## **Recommended Steps**

1. Review the below documents in this article to understand the different possible scenarios<br>
2. Review the [Current Azure Status](https://azure.microsoft.com/status/) or [Azure Status - History](https://azure.microsoft.com/status/history/) for outages
3. [Understand more about Resource Health Center](https://docs.microsoft.com/azure/resource-health/resource-health-overview) and using [Resource Health blade](data-blade:Microsoft_Azure_Health.resourcehealthdetailblade.resourceId.$resourceId) for any impactful events specific for your VM<br>
4. [Understand more about Audit logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview) and using [Audit and Activity Log blade](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter.subscriptionId.$subscriptionId)

## **Recommended Documents**

**Azure host server faults, unplanned maintenance, and other related scenarios**<br>

If the host server cannot reboot for any reason or detects a specific issue associated with your VM, the Azure platform initiates an auto-recovery action on either the impacted VMs or the host itself. This may take the faulty host server out of rotation for further investigation or the host will force the VM itself to restart.<br>

* [Host server faults](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#host-server-faults)<br>
* [Auto-recovery actions](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#auto-recovery)<br>
* [Unplanned maintenance](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#unplanned-maintenance)<br>
* [Storage-related forced shutdowns](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#storage-related-force)<br>

**User-initiated reboot or shutdown actions**

Customers often restart their VMs themselves but may not be aware that the action was performed. The articles below on how to identify this scenario yourself.<br>

* [Understanding user-initiated reboot or shutdown actions](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#user-initiated-reboot-or-shutdown-actions)<br>
* [Overview of Activity Logs to identify restart issues](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview)

**Planned maintenance and memory-reserving updates**<br>

To understand what Azure planned maintenance is and how it can affect the availability of your Linux VMs, see the articles listed below. The articles provide background about the Azure planned maintenance process and how to schedule planned maintenance to further reduce the impact.<br>

* [Understanding planned maintenance](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#planned-maintenance)<br>
* [Planned maintenance for VMs in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/planned-maintenance)<br>
* [How to schedule planned maintenance on Azure VMs](https://docs.microsoft.com/azure/virtual-machines/windows/planned-maintenance)<br>
* [Understanding memory-preserving updates](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#memory-preserving-updates)<br>
* [Use Azure redeploy functionality to transfer virtual machines to a new Azure node](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows)<br>

**Issues or actions from within the VM**<br>

* [Understanding more about VM crashes](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#vm-crashes)<br>
* [Understand Windows Update and Azure Security update installation](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#azure-security-center-and-windows-update)<br>
* [Diagnose & recover from boot failures after a restart](https://azure.microsoft.com/blog/boot-diagnostics-for-virtual-machines-v2/)
