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
## What is the best place to find more details on the vulnerability?
Please refer the Microsoft blog post [Securing Azure Customers from CPU vulnerability](https://azure.microsoft.com/blog/securing-azure-customers-from-cpu-vulnerability/) for more details.

## Is there a way to know when a particular VM will be rebooted?
Unfortunately not. The best way to get an alert about the impending reboot is to configure [Scheduled Events](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events). This will give a 15 minute notification of the VM going down due to maintenance. In addition, the activity log entry can be used to trigger Azure Monitor to send emails, SMS, or webhooks.

## Were there notifications sent out about the scheduled maintenance?
Yes, an email and an in-portal service health notification has been sent to all impacted subscriptions. The email went to subscription administrators and co-administrators. The in-portal service health notification resides in Azure Service Health and triggers any Azure Monitor alerts set to activate by the ‘service health’ category.

## I received a maintenance notice that looks very similar to the IaaS Virtual Machine notice from App Service/Azure Functions. Is it for the same maintenance?
No, we are rolling out a routine update to the underlying infrastructure of our Azure App Services. This will not impact IaaS VMs, Cloud Services, or any other Azure services, and is not associated with the Planned Host OS maintenance. <br>
We have since sent a follow up notification to customers' management portals to clarify that this is specific to app services and functions. During this update, there will be a brief restart of the web apps, similar to what occurs during the regular monthly OS update.

## How long will the reboot take?
We estimate completion with 30 - 45 minutes.

## Does the guest OS need to be updated?
No, its not required this time. The current Host updates will mitigate  this vulnerability. But we always recommend that customers maintain the latest patch levels on the guest OS. Please consult with the vendor of your operating systems for updates and instructions, as needed. For Windows Server VM customers, guidance has now been published and is available [here](https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/ADV180002).

## If I follow your recommendations for High Availability by using an Availability Set, am I safe?
Virtual machines deployed in an availability set or virtual machine scale sets have the notion of Update Domains (UD). When performing maintenance, Azure honors the UD constraint and will not reboot virtual machines from different UD (within the same availability set). Azure also waits for at least 30 minutes before moving to the next group of virtual machines.

For more information about high availability, please refer [Manage the availability of Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/manage-availability) and [Manage the availability of Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/manage-availability).

## I have architected my business continuity/disaster recovery plan using region pairs. Will reboots to my VMs occur in region pairs at the same time? 
Normally, Azure planned maintenance events are rolled out to paired regions one at a time to minimize the risk of disruption in both regions. However, due to the urgent nature of this security update, we are rolling the update out to all regions concurrently

## What is the experience in the case of Cloud Services (Web/Worker Role), Service Fabric, and Virtual Machine Scale Sets?
While these platforms are impacted by planned maintenance, customers using these platforms are considered safe given that only VMs in a single Upgrade Domain (UD) will be impacted at any given time.

## What if Service Health doesn’t show a VM, or is blank?
The column can take some time to load, so customers should wait to ensure that the page is fully loaded. If there are still blank statuses, no reboot is needed. The experience has been changed for the scheduled maintenance starting today. VMs only have two possible statuses: “Scheduled” or “Already updated”. Scheduled means that the VM will be impacted by planned maintenance, so customers should expect that this VM will be rebooted during scheduled maintenance. “Already updated” means that the VM does not require maintenance – either because it has already been rebooted, or because the VM was allocated to an already-updated host.

## Why is my VM scheduled for maintenance for the second time
There are several use cases where you will see your VM scheduled for maintenance after you have already completed your maintenance-redeploy:

* You VM was service healed to another node, which has not been updated yet, due to a hardware fault
* You stopped (deallocated​) and restarted the VM, and it landed on a host that was not updated.
* You have auto shutdown set on the VM, and when it restarted, it was placed on a host that was not yet updated

## Will there be a performance impact as a result of resolving this?
The majority of Azure customers should not see a noticeable performance impact with this update. We’ve worked to optimize the CPU and disk I/O path and are not seeing noticeable performance impact after the fix has been applied. A small set of customers may experience some networking performance impact. This can be addressed by turning on Azure Accelerated Networking (Windows, Linux), which is a free capability available to all Azure customers. We will continue to monitor performance closely and address customer feedback.

## **Recommended documents**
[Securing Azure customers from CPU vulnerability](https://azure.microsoft.com/en-us/blog/securing-azure-customers-from-cpu-vulnerability/)
[Understanding planned maintenance for Windows virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-and-updates)<br>
[How to view notifications and alerts in the portal](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#notification-and-alerts-in-the-portal)<br>
[How to view VMs scheduled for maintenance in the portal](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#view-vms-scheduled-for-maintenance-in-the-portal)<br>
[Check maintenance status using PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#check-maintenance-status-using-powershell)<br>
[What about Classic deployments?](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#classic-deployments)<br>
