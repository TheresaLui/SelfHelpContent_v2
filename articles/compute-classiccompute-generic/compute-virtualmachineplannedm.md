<properties
	pageTitle="planned maintenance/general questions or issues"
	description="planned maintenance/general questions or issues"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottazure"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32591320,32589415"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public"
/>

# Planned Maintenance/general questions or issues
**I don't see any indication of planned maintenance in the portal, Powershell, or CLI.**<br>

Information related to planned maintenance is available during a planned maintenance wave only for the VMs which are going to be impacted by it. In other words, if you see no data, it could be that the maintenance wave has already completed (or not started) or that your virtual machine is already hosted in an updated server.<br>

**What are the different possible values for my virtual machine?**

Value	| Description
--- | ---
Start now |The VM is in the self-service maintenance window which lets you initiate the maintenance yourself. See below on how to start maintenance on your VM
Scheduled	|The VM is scheduled for maintenance with no option for you to initiate maintenance. You can learn of the maintenance window by selecting the Auto-Scheduled window in this view or by clicking on the VM
Empty or Completed |You have successfully initiated and completed maintenance on your VM.
Skipped	|You have selected to initiate maintenance with no success. Azure has canceled the maintenance for your VM and will reschedule it in a later time

## **Recommended documents**
[Understanding planned maintenance for Windows virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-and-updates)<br>
[Handling planned maintenance notifications for Windows virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications)<br>
[In-depth FAQ for planned maintenance](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#faq)<br>
[How to view notifications and alerts in the portal](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#notification-and-alerts-in-the-portal)<br>
[How to view VMs scheduled for maintenance in the portal](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#view-vms-scheduled-for-maintenance-in-the-portal)<br>
[Check maintenance status using PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#check-maintenance-status-using-powershell)<br>
[What about Classic deployments?](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#classic-deployments)<br>
