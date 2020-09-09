<properties
	pageTitle="Virtual machine restarts"
	description="Virtual machine restarts"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,yareyes,amamun"	
	authors="ujpat,yareyes,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740114"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="ff1e30e2-71cd-4814-ad2f-08bd8c33b771"
	ownershipId="AzureData_AzureSQLVM"
/>


# Virtual machine restarts

4 out of 5 customers resolved their VM disk issue using the steps below.

## **Recommended Steps**

**[Azure Resource Health](https://docs.microsoft.com/azure/resource-health/resource-health-overview)** helps you diagnose and get support when an Azure service problem affects your resources. It informs you about the current and past health of your resources, and it provides technical support to help you mitigate problems. <br>

Where **[Azure Status](https://status.azure.com/)** informs you about service problems that affect a broad set of Azure customers, **[Resource Health](data-blade:Microsoft_Azure_Health.resourcehealthdetailblade.resourceId.$resourceId)** gives you a personalized dashboard of the health of your resources. Resource Health shows you all the times your resources were unavailable in the past because of Azure service problems.

1. Review [Resource Health blade](data-blade:Microsoft_Azure_Health.resourcehealthdetailblade.resourceId.$resourceId) for any impactful events specific for your VM<br>
2. Review the [Current Azure Status](https://azure.microsoft.com/status/) or [Azure Status - History](https://status.azure.com/status/history/) for outages<br>
3. [Understand more about Audit logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview) and using [Audit and Activity Log blade](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter.subscriptionId.$subscriptionId)

## **Recommended Documents**

**Azure host server faults, unplanned maintenance, and other related scenarios**<br>

If the host server cannot reboot for any reason or detects a specific issue associated with your VM, the Azure platform initiates an auto-recovery action on either the impacted VMs or the host itself. This may take the faulty host server out of rotation for further investigation or the host will force the VM itself to restart.<br>

* [Host server faults](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#host-server-faults)<br>
* [Auto-recovery actions](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#auto-recovery)<br>
* [Unplanned maintenance](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#unplanned-maintenance)<br>
* [Storage-related forced shutdowns](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#storage-related-force)

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
* [Use Azure redeploy functionality to transfer virtual machines to a new Azure node](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-windows)

**Issues or actions from within the VM**<br>

* [Understanding more about VM crashes](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#vm-crashes)<br>
* [Understand Windows Update and Azure Security update installation](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/understand-vm-reboot#azure-security-center-and-windows-update)<br>
* [Diagnose & recover from boot failures after a restart](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/boot-diagnostics)
