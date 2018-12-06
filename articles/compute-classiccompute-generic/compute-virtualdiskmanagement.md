<properties
	pageTitle="configuration and setup/virtual disk management"
	description="configuration and setup/virtual disk management"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	authorAlias="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32411841"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public"
/>

# Virtual Disk Management

4 out of 5 customers resolved their VM virtual disk issue using the below steps.<br>

**Need help wth attaching or detaching disks**<br>

* Learn how to **attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-a-new-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#add-an-empty-data-disk-to-a-virtual-machine)<br>
* Learn how to **attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-an-existing-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#attach-an-existing-data-disk-to-a-vm)<br>
* Learn how to **detach a data disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-the-portall) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-powershell).<br>
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/windows/find-unattached-disks)

	When detaching a VM, **remember** to connect to the VM and **unmount the disk first**.<br>

**Need help with Premium Storage (SSD)**<br>

* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)<br>
* [What VMs are supported for Premium Storage (SSD)](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#supported-vms)<br>
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#premium-disks-managed-and-unmanaged)

**Issue with increasing the size or resize a disk attached to the VM (OS or data disk)**<br>

* [Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm)<br>
* [How to expand the OS drive of a virtual machine](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk)
* [Resize data disks for a VM](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk#resizing-data-disks)<br>
* [Expand the disk partition after expanding the virtual hard disk](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk)<br>

**Need help with Managed Disks or conversion from unmanaged**<br>

* [Overview of Azure Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview)<br>
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks)<br>
* [Plan for the conversion to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/linux/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)<br>
* [Convert a VM from unmanaged disks to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)<br>
* [FAQ for migrating to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#migrate-to-managed-disks)

## **Other Recommended Documents**

* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)<br>
* [Understanding the temporary drive on your VM](https://docs.microsoft.com/azure/storage/storage-about-disks-and-vhds-linux#temporary-disk)
