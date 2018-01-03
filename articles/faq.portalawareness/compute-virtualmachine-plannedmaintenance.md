<properties
	pageTitle="FAQ for Azure Planned Maintenance"
	description="FAQ for Azure Planned Maintenance"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottazure"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="99999999"
	resourceTags=""
	productPesIds="99999"
	cloudEnvironments="public"
/>

# **FAQs**
## Why didn't Azure announce this planned maintenance earlier?
Azure has been investing in technologies such as In-place Migration (aka Preserving Host Update) that enables us to roll out many changes to the Azure Hosting infrastructure with only a few seconds of VM downtime while maintaining memory, open files, and network connections. We've been using this technique for the majority of updates to the Azure hosting infrastructure such security patches as well as to roll out many improvements and new capabilities to the platform, however, there are cases where we can't avoid rebooting virtual machines hosted in Azure. Since our last large-scale Azure host update that needed a VM reboot in early 2016, we have accumulated several changes which require us to restart our servers which will result in virtual machines reboot.<br>
Azure strives to give its customers as much advanced notice on any planned maintenance activity. Due to the importance of this update, the notification timeline for this planned maintenance wave is shorter than usual.
This maintenance will update the host operating system as well as Firmware and BIOS of the host. These critical updates will assist us in improving monitoring, security, availability, serviceability, and performance of the Azure infrastructure. 
Azure understands that any planned maintenance is impactful to our customers business and is committed to further reduce the frequency and scope of such impactful planned maintenance activity by continuing to invest in non-disruptive maintenance technology.

## Can my VM be exempt from reboot during the scheduled maintenance phase? 
The new Planned Maintenance experience was enabled to provide customers more control over the maintenance. This includes a self-service maintenance window where customers have the option to pro-actively redeploy their VMs to an already update host, followed by a scheduled maintenance window where Azure will force reboot all remaining VMs.

The current maintenance schedule has been created considering a wide range of factors to reduce the impact as much as possible. Unfortunately, it is not possible to modify the given start and end times, schedule a particular reboot time for a VM during the scheduled maintenance phase or exempt a VM from this maintenance. We apologize for any inconvenience that this might create.

## How long will it take to finish self-service maintenance on my virtual machine?
If you initiate self-service maintenance on your virtual machine, the platform will move your VM from its current host to a new, already updated host. This process only takes several minutes for single instance VMs. 

## Is there a way to know exactly when my virtual machine will be impacted?
The Azure initiated reboot during the scheduled maintenance phase can happen anytime during the indicated maintenance window. The exact sequencing of servers (and VMs) within this window is unknown. However, it should be expected that the reboot will occur more towards the beginning of the window for the vast majority of resources. The only way to get an indication of the reboot about to happen is via Scheduled events,  which surfaces an event 15 minutes prior to the reboot occurring. This can be used to programmatically initiate failover to another resource or migrate activities.

## How long will it take you to reboot my virtual machine during the scheduled maintenance phase?
The Azure initiated reboot during the scheduled maintenance phase is typically completed within 25 minutes, but could take up to 45 minutes for some instance.

## How are availability sets impacted during scheduled maintenance window?
Virtual machines deployed in an availability set or virtual machine scale sets have the notion of Update Domains (UD). When performing maintenance, Azure honors the UD constraint and will not reboot virtual machines from different UD.<br>
Azure triggers maintenance on availability sets by update domain. All VMs in one Update Domain will be updated at the same time. There will be 30 minutes pause between each group of VMs in different Update Domains in order to allow VM instances to fully recover before the next Update Domain starts maintenance.

## What will be the experience in the case of cloud services and scale sets?
While these platforms are impacted by planned maintenance, customers using these platforms are considered safe given that only VMs in a single Upgrade Domain (UD) will be impacted at any given time. Customer initiated maintenance is currently not available for Cloud Services and virtual machine scale sets.

## How can I find out about the details of the maintenance schedule of my VM?
The status as well as the maintenance window of the VMs can be checked in the Azure Health Dashboard in the Portal as well as VM list view or via PowerShell/CLI. These interfaces reflect the up-to-date status. The How-To Guide for [Windows](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/maintenance-notifications) and [Linux](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/maintenance-notifications) VMs includes more detailed information on the maintenance status and other important aspects of planned maintenance including on how to initiate maintenance from the Azure Portal and CLI/PowerShell.

## Why does my VM status show "Failed" and the maintenance status shows "Completed", but my VM is running fine?
This is likely due to a long running maintenance update that resulted in an incorrect VM status being shown. To update this status, please add a "Tag" to the VM and let the system update. The VM status should then reflect the correct status again and the tag can be removed

## Why do some or all of my VMs not show any maintenance status or schedule?
VMs might not show a maintenance status or schedule in the portal or PowerShell/CLI due to one of the following reasons:

* VM is a Cloud Services or Virtual Machine Scale Set instance
* VM is currently stopped/deallocated. Those VMs are not assigned to a host. Once they get started and a host is allocated it will reflect the maintenance status based on the then current host.
* VMs are already on an updated host and therefore will not be impacted by this maintenance wave.
* Please check if you have ‘maintenance’ column added to your VM list view in the portal. While we have added this column to the default view, customers who configured their current view to display any non-default columns must manually add the Maintenance column to their VM list view.

## Will the IP address and/or MAC address have changed after the maintenance update?
Dynamic IP addresses are released when the vm is stopped or deleted. So during the self-service maintenance or forced reboot of the VM for scheduled maintenance dynamic IPs would be released and new IPs would be assigned once the VM is up.<br>
Static IP addresses are released only when the vm is deleted and so are not impacted during maintenance.<br>
MAC address are only changed when a new NIC is assigned to VM and this is not expected to happen during maintenance.

## **Recommended documents**
[Understanding planned maintenance for Windows virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-and-updates)<br>
[Handling planned maintenance notifications for Windows virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications)<br>
[In-depth FAQ for planned maintenance](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#faq)<br>
[How to view notifications and alerts in the portal](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#notification-and-alerts-in-the-portal)<br>
[How to view VMs scheduled for maintenance in the portal](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#view-vms-scheduled-for-maintenance-in-the-portal)<br>
[Check maintenance status using PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#check-maintenance-status-using-powershell)<br>
[What about Classic deployments?](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#classic-deployments)<br>
