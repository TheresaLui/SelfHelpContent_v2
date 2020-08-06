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
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="5f467c0f-7f88-4a63-9496-4cf72c764cf9"
	ownershipId="Compute_VirtualMachines"
/>

# Virtual Disk Management

4 out of 5 customers resolved their VM virtual disk issue using the below steps.

**Attaching or Detaching Disks**

* **Attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-a-new-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-a-new-disk-to-a-vm)
* **Attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-an-existing-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-an-existing-disk)
* **Detach a data disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-the-portal) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-azure-cli)
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/linux/find-unattached-disks)

**NOTE**: When detaching a VM, remember to connect to the VM and **unmount the disk first**.

**Premium Storage (SSD)**

* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#features)
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#supported-vms)
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/linux/faq-for-disks#premium-disks-managed-and-unmanaged)

**Increase or resize a disk attached to the VM (OS or data disk)**

* [Expand virtual hard disks with Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/expand-disks)
* [Expand a disk partition and filesystem after expanding the virtual hard disk](https://docs.microsoft.com/azure/virtual-machines/linux/expand-disks#expand-a-disk-partition-and-filesystem)

**Managed Disks or conversion from unmanaged**

* [Overview of Azure Managed Disks](https://docs.microsoft.com/azure/virtual-machines/linux/managed-disks-overview)
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks)
* [Plan for the conversion to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)
* [Convert a VM from unmanaged disks to managed disks](https://docs.microsoft.com/azure/virtual-machines/linux/convert-unmanaged-to-managed-disks)
* [FAQ for migrating to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/linux/faq-for-disks#migrate-to-managed-disks)

## **Recommended Documents**

* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)
* [Learn how to resize a VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size)
* [Understanding the temporary drive on your VM](https://docs.microsoft.com/azure/storage/storage-about-disks-and-vhds-linux#temporary-disk)
