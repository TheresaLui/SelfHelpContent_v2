<properties
	pageTitle="planned maintenance/general questions or issues"
	description="planned maintenance/general questions or issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottazure"
    ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public"
	articleId="49955c3a-0bc9-41a9-8520-8c6fbe81b4cb"
/>

# Planned Maintenance/general questions or issues

**I don't see any indication of planned maintenance in the portal, PowerShell, or CLI.**<br>

Information related to planned maintenance is provided only during a planned maintenance wave. For Azure Virtual Machine Scale Sets (VMSS), the planned maintenance performs updates to improve the reliability, performance, and security of the host infrastructure for the VMs.

If you have received no notifications, it could be that the maintenance wave has already completed or scheduled for another time.

Maintenance is performed primarily on the hosting environment, and only affects the individual VMs when upgrading and decommissioning hardware is warranted. You will be notified only if one or more of the VMs in a VMSS requires a reboot.

If a reboot is required, Azure uses in-place migration to pause the VM while the host is updated. These operations are applied across fault domains. Operations are stopped if any warning health signals are received.<br>

If a reboot is not required, you will receive a notification that shows when a planned maintenance wave is planned. You are given a time window in which you can determine which VMs are included in the wave and the start time.<br>

If you are considering performing self-service maintenance, be aware that self-service maintenance might not be available for all your VMs and is not recommended for deployments using availability sets.<br>

See [Planned maintenance notifications for virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-maintenance-notifications#view-virtual-machine-scale-sets-that-are-affected-by-maintenance-in-the-portal) for information on the following:

- Determining which VM Scale Sets are affected by the planned maintenance
- Starting the planned maintenance
- Checking the maintenance status using PowerShell or the Azure CLI<br>

**What are the different possible values for my VMSS during planned maintenance?**<br>

The maintenance status information provides the following data:

- The beginning and end times of the planned maintenance scheduled in which Azure initiates maintenance on your VM.
- The beginning and end of the maintenance self-service window when you can initiate maintenance on your VM.
- The result of the last attempt to initiate maintenance on the VM.<br>

## **Recommended documents**

* [Planned maintenance notifications for virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-maintenance-notifications#view-virtual-machine-scale-sets-that-are-affected-by-maintenance-in-the-portal)
