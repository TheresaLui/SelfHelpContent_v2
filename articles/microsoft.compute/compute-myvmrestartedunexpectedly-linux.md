<properties
	pageTitle="Resolve issues with an unexpected Linux VM restart"
	description="Resolve issues with an unexpected Linux VM restart"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder="53"
	selfHelpType="resource"
	supportTopicIds="32628269,32628280,32628287"
	resourceTags="linux, redhat, Ubuntu"
	productPesIds="15797,15571,16470,16454,16342"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="ccda7af8-571e-48ad-9b1e-63b0b2a3101b"
	ownershipId="Compute_VirtualMachines"
/>

# Resolve issues with an unexpected Linux VM restart

4 out of 5 customers resolved their VM restart issue using the steps below.<br>

## **Recommended Steps**

**[Azure Resource Health](https://docs.microsoft.com/azure/resource-health/resource-health-overview)** helps you diagnose and get support when an Azure service problem affects your resources. It informs you about the current and past health of your resources, and it provides technical support to help you mitigate problems. <br>

Where **[Azure Status](https://status.azure.com/)** informs you about service problems that affect a broad set of Azure customers, **[Resource Health](data-blade:Microsoft_Azure_Health.resourcehealthdetailblade.resourceId.$resourceId)** gives you a personalized dashboard of the health of your resources. Resource Health shows you all the times your resources were unavailable in the past because of Azure service problems.

1. Review [Resource Health blade](data-blade:Microsoft_Azure_Health.resourcehealthdetailblade.resourceId.$resourceId) for any impactful events specific for your VM<br>
2. Review the [Current Azure Status](https://status.azure.com/status/) or [Azure Status - History](https://status.azure.com/status/history/) for outages<br>
3. [Understand more about Audit logs](https://docs.microsoft.com/azure/azure-monitor/platform/activity-logs-overview) and using [Audit and Activity Log blade](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter.subscriptionId.$subscriptionId)

## **Recommended Documents**

* [Understand and use Resource Health Center to troubleshoot this scenario in the future](https://docs.microsoft.com/azure/resource-health/resource-health-overview)<br>
* [How to view VM reboot logs to identify the cause of reboot](https://azure.microsoft.com/blog/viewing-vm-reboot-logs)<br>
* [Diagnose & recover from boot failures after a restart](https://azure.microsoft.com/blog/boot-diagnostics-for-virtual-machines-v2/)<br>
* [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/linux/manage-availability)<br>
* [Configure availability sets for virtual machines with Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/tutorial-availability-sets)<br>
* [Understand planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/maintenance-and-updates)<br>
* [Service Healing - Auto-recovery of Virtual Machines](https://azure.microsoft.com/blog/service-healing-auto-recovery-of-virtual-machines)<br>
* [Use Azure redeploy functionality to transfer virtual machines to a new Azure node](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/redeploy-to-new-node-linux)
