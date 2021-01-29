<properties
  pagetitle="Planned maintenance for Host infrastructure"
  service="microsoft.compute"
  resource=""
  ms.author="scotro,babhoo"
  selfhelptype="Generic"
  supporttopicids="32783376,32783377,32783378,32783379"
  resourcetags=""
  productpesids="16080"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="49955c3a-0bc9-41a9-8520-8c6fbe81b4cb"
  ownershipid="Compute_VirtualMachineScaleSets_Content"
/>

# Resolve issues with Azure Planned Maintenance

On virtual machine scale sets, Azure provides planned maintenance options for both host infrastructure updates and guest OS image updates. 

## Planned maintenance for host infrastructure

To maintain the host infrastructure, Azure applies impactless updates fault domain by fault domain. VMs in the scale sets are paused while their hosts are updated. No notifications are sent for these operations. Certain very sensitive workloads can be impacted by these updates. If you have such a workload, you can control all updates by using Azure Dedicated Host or Isolated VM.

For any update that causes reboot to the VM instances within the scale sets, planned maintenance is scheduled in waves. A wave starts with a notification to a subscription owner and co-owners. This notification defines a schedule with two time windows:

- **Self-service window**<br>
- **Scheduled maintenance window**<br>

The self-service window is when you can proactively start self-service maintenance. Be aware that self-service maintenance might not be available for all your VMs, and is also not recommended for VMs in availability sets.<br>

After the self-service window ends, Azure schedules a time in the scheduled maintenance window to apply the required maintenance to your VM (provided the work has not been already performed by self-service).<br>

If you don't see notifications, it could due to of the following reasons:<br>

- The maintenance wave is finished<br>
- The maintenance wave has not started<br>
- The VM is hosted on an updated server<br>
- The VM is deployed to a region where planned maintenance is already complete or not required.<br>

For more information, see [Planned maintenance notifications for virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-maintenance-notifications#view-virtual-machine-scale-sets-that-are-affected-by-maintenance-in-the-portal) which covers the following:<br>

- Notifications and alerts about planned maintenance<br>
- Schedules for the planned maintenance and self-service windows<br>
- VM scale sets affected by the planned maintenance<br>
- Instructions and guidelines for using  self-service maintenance<br>
- Status queries using Azure CLI and PowerShell<br>
- Frequently asked questions<br>

## Maintenance control for guest OS image updates 

Maintenance control lets you decide when to apply updates to guest OS disks in your virtual machine scale sets through an easier and more predictable experience. 

The entire workflow comes down to these steps:
- Create a maintenance configuration
- Associate a virtual machine scale set to a maintenance configuration
- Enable automatic OS upgrades

During your defined scheduled window, Azure performs OS image upgrade for the instances of your virtual machine scale sets. For now, only a daily window is supported and the duration of the window must be 5 hours.

## **Recommended Documents**

* [Planned maintenance notifications for virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-maintenance-notifications#view-virtual-machine-scale-sets-that-are-affected-by-maintenance-in-the-portal)<br>
* [Working with large virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-placement-groups)<br>
* [Azure Metadata Service: Scheduled Events for Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/scheduled-events)<br>
* [Regions and availability for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/regions)<br>
* [Choosing the right number of fault domains for virtual machine scale set](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-manage-fault-domains)<br>
* [Azure virtual machine scale sets FAQs](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-faq)
* [Azure virtual machine scale set automatic OS image upgrades](https://docs.microsoft.com/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-automatic-upgrade)
* [Maintenance control for Azure virtual machine scale sets](https://docs.microsoft.com/azure/virtual-machines/virtual-machine-scale-sets-maintenance-control)
