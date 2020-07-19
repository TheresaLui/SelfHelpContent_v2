<properties
    pageTitle="My VM restarted unexpectedly"
    description="My VM restarted unexpectedly "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="ScottAzure"
    ms.author="scotro
    displayOrder="8"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="windows,windowsSQL"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="ea8323dd-e3ed-454c-9c78-158bd2c430b9"
	ownershipId="Compute_VirtualMachines"
/>

# My VM restarted unexpectedly

## **Recommended Steps**

The common reasons for a VM restarting are:

* Azure caused (planned or unplanned maintenance or outage) or issues with the operating system or application

The following are steps to find out the reason for a restart in the past and to mitigate for future occurrences:

1. Review [Audit Logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter.subscriptionId.$subscriptionId) for the time period of the restart to determine the reason
2. [Understand, manage, and use 'Availability Sets' to reduce the impact of downtime events](https://docs.azure.cn/virtual-machines/windows/manage-availability)

## **Recommended Documents**

* [How to view VM reboot logs to identify the cause of reboot](https://azure.microsoft.com/blog/viewing-vm-reboot-logs)<br>
* [Diagnose & recover from boot failures after a restart](https://azure.microsoft.com/blog/boot-diagnostics-for-virtual-machines-v2/)<br>
* [Manage the availability of virtual machines](https://docs.azure.cn/virtual-machines/windows/manage-availability)<br>
* [Configure availability sets for Windows virtual machines in classic deployments](https://docs.azure.cn/virtual-machines/windows/classic/configure-availability)<br>
* [Configure availability sets for Windows virtual machines using Resource Manager deployments](https://docs.azure.cn/virtual-machines/windows/create-availability-set?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)<br>
* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.azure.cn/service-health/resource-health-overview)<br>
* [Understand planned maintenance and how it is communicated for virtual machines in Azure](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)<br>
* [Service Healing - Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)<br>
* [Use Azure redeploy functionality to transfer virtual machines to a new host](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)
