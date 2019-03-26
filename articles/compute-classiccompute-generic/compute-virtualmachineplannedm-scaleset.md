<properties
	pageTitle="planned maintenance/general questions or issues"
	description="planned maintenance/general questions or issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottazure"
    ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32589415"
	resourceTags=""
	productPesIds="16080"
	cloudEnvironments="public"
	articleId="49955c3a-0bc9-41a9-8520-8c6fbe81b4cb"
/>

# Planned Maintenance in virtual machine scale sets

**I don't see any indication of planned maintenance in the portal, PowerShell, or CLI.**<br>

Azure conducts planned maintenance on virtual machine scale sets. To maintain the host infrastructure, Azure uses in-place migration to apply updates across fault domains. VMs in the scale sets are paused while their hosts are updated. No notifications are sent for these operations.<br>

To maintain the VM instances within the scale sets, planned maintenance is scheduled in waves. A wave starts with a notification to a subscription owner and co-owners. This notification defines a schedule with two time windows:

- **Self-service window**
- **Scheduled maintenance window**<br>

The self-service window is when you can proactively start self-service maintenance. Be aware that self-service maintenance might not be available for all your VMs, and is also not recommended for VMs in availability sets.

After the self-service window ends, Azure schedules a time in the scheduled maintenance window to apply the required maintenance to your VM (provided the work has not been already performed by self-service).<br>

If you don't see notifications, it could due to of the following reasons:

- The maintenance wave is finished
- The maintenance wave has not started
- The VM is hosted on an updated server
- The VM is deployed to a region where planned maintenance is already scheduled

For more information, see [Planned maintenance notifications for virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-maintenance-notifications#view-virtual-machine-scale-sets-that-are-affected-by-maintenance-in-the-portal) which covers the following:

- Notifications and alerts about planned maintenance
- Schedules for the planned maintenance and self-service windows
- VM scale sets affected by the planned maintenance
- Instructions and guidelines for using  self-service maintenance
- Status queries using Azure CLI and PowerShell
- Frequently asked questions

## **Recommended Documents**

* [Planned maintenance notifications for virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-maintenance-notifications#view-virtual-machine-scale-sets-that-are-affected-by-maintenance-in-the-portal)<br>
* [Working with large virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-placement-groups)<br>
* [Azure Metadata Service: Scheduled Events for Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events)<br>
* [Regions and availability for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/regions-and-availability)<br>
* [Choosing the right number of fault domains for virtual machine scale set](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-manage-fault-domains)<br>
* [Azure virtual machine scale sets FAQs](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-faq)
