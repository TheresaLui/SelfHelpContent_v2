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

# Planned Maintenance/general questions or issues

**I don't see any indication of planned maintenance in the portal, PowerShell, or CLI.**<br>

Information related to planned maintenance is provided only during a planned maintenance wave. For Azure Virtual Machine Scale Sets (VMSS), the planned maintenance performs updates to improve the host infrastructure for the VMs. You are notified only if one or more of the VMs in a VMSS requires a reboot.<br>

Maintenance is performed primarily on the hosting environment, and affects the individual VMs only when upgrading and decommissioning hardware.<br>

If you haven't received any notifications, it could be that the maintenance wave has completed or is scheduled for a later time.<br>

If a reboot is not required, Azure uses in-place migration to pause the VM while the host is updated. Maintenance operations are applied across fault domains. Progress is stopped if any warning health signals are received.<br>

If a reboot is required, you'll receive a notification that shows when the maintenance is planned. You are given a time window when you can start the maintenance at a time that works best for you.<br>

If you are considering performing self-service maintenance, be aware that it might not be available for all your VMs and is also not recommended for deployments using availability sets. See [Planned maintenance notifications for virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-maintenance-notifications#view-virtual-machine-scale-sets-that-are-affected-by-maintenance-in-the-portal) for information on about these considerations and the following:<br>

- Determining which VM Scale Sets are affected by the planned maintenance
- Starting the planned maintenance
- Checking the maintenance status using PowerShell or the Azure CLI<br>

**What are the different possible values for my VMSS during planned maintenance?**<br>

The maintenance status information provides the following data:

- The beginning and end times of the planned maintenance scheduled for  your VMs.
- The beginning and end of the maintenance self-service window when you can initiate maintenance on your VMs.
- The result of the last attempt to initiate maintenance on a VM.<br>

## **Recommended documents**

* [Planned maintenance notifications for virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-maintenance-notifications#view-virtual-machine-scale-sets-that-are-affected-by-maintenance-in-the-portal)
* [Working with large virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-placement-groups)
* [Azure virtual machine scale sets FAQs](https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-faq)
