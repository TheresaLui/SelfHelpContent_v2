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
# Planned Maintenance FAQ
## **Overview**
An industry-wide, hardware-based security vulnerability was [disclosed on January 3](https://googleprojectzero.blogspot.com/2018/01/reading-privileged-memory-with-side.html). As part of Microsoft’s commitment to security, we are taking actions to ensure that no Azure customer is exposed to these vulnerabilities, including accelerating our execution of the January planned maintenance.

**The planned maintenance is now completed across to our entire fleet**. During the maintenance some virtual machines may have experienced unexpected reboots. Additional information about the maintenance is available for [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/accelerated-maintenance) and [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/accelerated-maintenance) Virtual Machines.

We encourage you to read [our blog] (https://azure.microsoft.com/blog/securing-azure-customers-from-cpu-vulnerability/)  to learn more about our efforts to secure customers from the CPU vulnerabilities. 

## **Questions most frequently submitted to our support team**

### **How can I see which of my VMs are already updated?**
You can see the status of your VMs, and if the reboot completed, in the [VM list in the Azure portal](https://aka.ms/T08tdc). Your VMs are listed as either “Already updated” if the update has been applied, or “Scheduled” if the update is still required. If you want to see just your VMs “Scheduled” refer to your [Azure Service Health](https://portal.azure.com/).

### **How long will the reboot take?**
We estimate completion with 30 - 45 minutes.

### **What if Service Health doesn’t show a VM, or is blank?**
The column can take some time to load, so customers should wait to ensure that the page is fully loaded. If there are still blank statuses, no reboot is needed.

### **Is there a way to know when a particular VM will be rebooted?**
Unfortunately not. The best way to get an alert about the impending reboot is to configure [Scheduled Events](https://docs.microsoft.com/azure/virtual-machines/windows/scheduled-events). This will give a 15 minute notification of the VM going down due to maintenance.

### **Were there notifications sent out about the scheduled maintenance?**
Yes, an email and an in-portal service health notification has been sent to all impacted subscriptions. The email went to subscription administrators and co-administrators. The in-portal service health notification resides in Azure Service Health and triggers any Azure Monitor alerts set to activate by the ‘service health’ category.

### **Does the guest OS need to be updated?**
No, its not required this time. The current Host updates will mitigate this vulnerability. But we always recommend that customers maintain the latest patch levels on the guest OS. Please consult with the vendor of your operating systems for updates and instructions. For Windows Server VM customers, guidance has now been published and is available [here](https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/ADV180002).

### **Why is my VM scheduled for maintenance for the second time**
There are several use cases where you will see your VM scheduled for maintenance after you have already completed your maintenance-redeploy:

* You VM was service healed to another node, which has not been updated yet, due to a hardware fault
* You stopped (deallocated​) and restarted the VM, and it landed on a host that was not updated.
* You have auto shutdown set on the VM, and when it restarted, it was placed on a host that was not yet updated

### **Will there be a performance impact as a result of resolving this?**
The majority of Azure customers should not see a noticeable performance impact with this update. We’ve worked to optimize the CPU and disk I/O path and are not seeing noticeable performance impact after the fix has been applied. A small set of customers may experience some networking performance impact. This can be addressed by turning on Azure Accelerated Networking (Windows, Linux), which is a free capability available to all Azure customers. We will continue to monitor performance closely and address customer feedback.

### **I have architected my business continuity/disaster recovery plan using region pairs. Will reboots to my VMs occur in region pairs at the same time?**
Normally, Azure planned maintenance events are rolled out to paired regions one at a time to minimize the risk of disruption in both regions. However, due to the urgent nature of this security update, we are rolling the update out to all regions concurrently

### **I received a maintenance notice that looks very similar to the IaaS Virtual Machine notice from App Service/Azure Functions. Is it for the same maintenance?**
No, we are rolling out a routine update to the underlying infrastructure of our Azure App Services. This will not impact IaaS VMs, Cloud Services, or any other Azure services, and is not associated with the Planned Host OS maintenance. <br>
We have since sent a follow up notification to customers' management portals to clarify that this is specific to app services and functions. During this update, there will be a brief restart of the web apps, similar to what occurs during the regular monthly OS update.

### **What is the experience in the case of Cloud Services (Web/Worker Role), Service Fabric, and Virtual Machine Scale Sets?**
While these platforms are impacted by planned maintenance, customers using these platforms are considered safe given that only VMs in a single Upgrade Domain (UD) will be impacted at any given time.

## **Recommended documents**
[Securing Azure customers from CPU vulnerability](https://azure.microsoft.com/blog/securing-azure-customers-from-cpu-vulnerability/)
[Understanding planned maintenance for Windows virtual machines](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-and-updates)<br>
[How to view notifications and alerts in the portal](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#notification-and-alerts-in-the-portal)<br>
[How to view VMs scheduled for maintenance in the portal](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#view-vms-scheduled-for-maintenance-in-the-portal)<br>
[Check maintenance status using PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#check-maintenance-status-using-powershell)<br>
[What about Classic deployments?](https://docs.microsoft.com/azure/virtual-machines/windows/maintenance-notifications#classic-deployments)<br>
