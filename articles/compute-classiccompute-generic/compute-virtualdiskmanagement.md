<properties
	pageTitle="Virtual Disk Management"
	description="Virtual Disk Management"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32411841"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="836ed3ad-2dbf-4c5e-857e-a8659cea73b4"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Virtual Disk Management

4 out of 5 customers resolved their VM virtual disk issue using the below steps.

**Attaching or detaching disks**

* **Attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-a-new-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#add-an-empty-data-disk-to-a-virtual-machine)
* **Attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-an-existing-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#attach-an-existing-data-disk-to-a-vm)
* **Detach a data disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-the-portall) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-powershell)
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/windows/find-unattached-disks)

**NOTE**: When detaching a VM, remember to connect to the VM and **unmount the disk first**.

**Premium Storage (SSD)**

* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#supported-vms)
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#premium-disks-managed-and-unmanaged)

**Increase or resize a disk attached to the VM (OS or data disk)**

* [Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm)
* [Resize data disks for a VM](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk#resizing-data-disks)
* [How to expand the OS drive of a virtual machine](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk)
* [Expand the volume within the OS after expanding the virtual hard disk](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk)

**Managed Disks or conversion from unmanaged**

* [Overview of Azure Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview)
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks)
* [Plan for the conversion to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)
* [Convert a VM from unmanaged disks to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)
* [FAQ for migrating to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#migrate-to-managed-disks)

## **Recommended Documents**

* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)
* [Understanding the temporary drive on your VM](https://docs.microsoft.com/azure/storage/storage-about-disks-and-vhds-linux#temporary-disk)
