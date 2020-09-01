<properties
	pageTitle="planned maintenance/general questions or issues"
	description="planned maintenance/general questions or issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32589415"
	resourceTags=""
	productPesIds="15571, 15797, 16454,16470"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="249cdea5-5761-4150-8572-8978204e0991"
	ownershipId="Compute_VirtualMachines"
/>

# Planned Maintenance/general questions or issues

**I don't see any indication of planned maintenance in the portal, Powershell, or CLI.**<br>

Information related to planned maintenance is available during a planned maintenance wave only for the VMs which are going to be impacted by it. In other words, if you see no data, it could be that the maintenance wave has already completed (or not started) or that your virtual machine is already hosted in an updated server.<br>

**What are the different possible values for my virtual machine during planned maintenance?**<br>

* **Start now**: The VM is in the self-service maintenance window which lets you initiate the maintenance yourself
* **Scheduled**: The VM is scheduled for maintenance with no option for you to initiate maintenance. You can learn of the maintenance window by selecting the Auto-Scheduled window in this view or by clicking on the VM.<br>
* **Empty or Completed**: Your VM does not require any maintenance and no maintenance reboot will occur
* **Skipped**: You have selected to initiate maintenance with no success. You will not be able to utilize the Customer Initiated Maintenance option. Your VM will be rebooted by Azure during the scheduled maintenance phase.<br>

**For hardware that is decommissioned, is capacity impacted?**
No, Azure Capacity isn't impacted as decommisioning hardware is planned.

## **Recommended Documents**

* [In-depth FAQ for planned maintenance](https://docs.microsoft.com/azure/virtual-machines/linux/maintenance-notifications#faq)<br>
* [Understanding planned maintenance for Linux virtual machines](https://docs.microsoft.com/azure/virtual-machines/linux/maintenance-and-updates)<br>
* [Handling planned maintenance notifications for Linux virtual machines](https://docs.microsoft.com/azure/virtual-machines/linux/maintenance-notifications)<br>
* [How to subscribe to notifications before any VM maintenance is performed](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events)<br>
* [How to view notifications and alerts in the portal](https://docs.microsoft.com/azure/virtual-machines/linux/maintenance-notifications#notification-and-alerts-in-the-portal)<br>
* [View VMs scheduled for maintenance in the portal](https://docs.microsoft.com/azure/virtual-machines/linux/maintenance-notifications#view-vms-scheduled-for-maintenance-in-the-portal)<br>
* [Find VMs scheduled for maintenance using CLI](https://docs.microsoft.com/azure/virtual-machines/linux/maintenance-notifications#find-vms-scheduled-for-maintenance-using-cli)<br>
* [Check maintenance status using CLI](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#check-maintenance-status-using-powershell)<br>
* [What about Classic deployments?](https://docs.microsoft.com/azure/virtual-machines/linux/maintenance-notifications#classic-deployments)
