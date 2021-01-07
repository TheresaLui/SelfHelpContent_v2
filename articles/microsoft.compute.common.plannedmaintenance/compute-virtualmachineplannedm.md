<properties
	pageTitle="Resolve issues with Azure planned maintenance"
	description="Resolve issues with Azure planned maintenance"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottazure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32783825,32783826,32783827,32783828"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="34c058c7-41ad-4a51-90da-d31ce8fe0ecf"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Resolve issues with Azure planned maintenance

**I don't see any indication of planned maintenance in the portal, Powershell, or CLI<br>**

Information related to planned maintenance is available during a planned maintenance wave only for the VMs which are going to be impacted by it. In other words, if you see no data, it could be that the maintenance wave has already completed (or not started) or that your virtual machine is already hosted in an updated server.<br>

**What are the different possible values for my virtual machine during planned maintenance?**

* **Start now**: The VM is in the self-service maintenance window which lets you initiate the maintenance yourself.<br>
* **Scheduled**: The VM is scheduled for maintenance with no option for you to initiate maintenance. You can learn of the maintenance window by selecting the Auto-Scheduled window in this view or by clicking on the VM.<br>
* **Already Updated**: Your VM does not require any maintenance and no maintenance reboot will occur.<br>
* **Retry Later**: You have initiated maintenance with no success. You will be able to use the self-service maintenance option at a later time.<br>
* **Retry Now**: You can retry a previously unsuccessful self-initiated maintenance.<br>
* **Skipped**: You have selected to initiate maintenance with no success. You will not be able to utilize the Customer Initiated Maintenance option. Your VM will be rebooted by Azure during the scheduled maintenance phase.<br>

**For hardware that is decommissioned, is capacity impacted?**
No, Azure Capacity isn't impacted as decommisioning hardware is planned.

## **Recommended Documents**

* [In-depth FAQ for planned maintenance](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#faq)<br>
* [Understanding planned maintenance for Windows virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-and-updates)<br>
* [How to view notifications and alerts in the portal](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#notification-and-alerts-in-the-portal)<br>
* [How to subscribe to notifications before any VM maintenance is performed](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events)<br>
* [Handling planned maintenance notifications for Windows virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications)<br>
* [How to view VMs scheduled for maintenance in the portal](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#view-vms-scheduled-for-maintenance-in-the-portal)<br>
* [Check maintenance status using PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#check-maintenance-status-using-powershell)<br>
* [What about Classic deployments?](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#classic-deployments)<br>
