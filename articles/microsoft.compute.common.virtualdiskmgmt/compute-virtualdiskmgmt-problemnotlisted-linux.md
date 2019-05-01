<properties
	pageTitle="Resolving issues with VM Disk Management"
	description="Resolving issues with VM Disk Management"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure,timbasham"
	ms.author="scotro,tibasham"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632141"
	resourceTags=""
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="public"
	articleId="compute-virtualdiskmgmt-problemnotlisted-linux"
/>

# Resolving issues with VM Disk Management

4 out of 5 customers resolved their VM disk issue using the steps below.

## **Recommended Steps**

### Attaching or detaching disks

* **Attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-a-new-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-a-new-disk-to-a-vm)<br>
* [Intialize a new data disk in a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#connect-to-the-linux-vm-to-mount-the-new-disk)<br>
* **Attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-an-existing-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-an-existing-disk)<br>
* **Detach a data disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-the-portal) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-azure-cli)<br>
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/linux/find-unattached-disks)<br>
* [Understanding the temporary disk on a VM](https://docs.microsoft.com/azure/storage/storage-about-disks-and-vhds-linux#temporary-disk)

**NOTE**: When detaching a disk, remember to connect to the VM and **unmount the disk first**.

### Premium Storage (SSD)

* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#features)
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#supported-vms)
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/linux/faq-for-disks#premium-disks-managed-and-unmanaged)

### Increase or resize a disk attached to the VM (OS or data disk)

* [How to expand the disk of a Linux VM](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/expand-disks)<br>
* [Resize a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size)<br>
* [Convert between Standard and Premium storage for a disk](https://docs.microsoft.com/azure/virtual-machines/linux/convert-disk-storage)<br>
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#supported-vms)<br>
* [Expand a volume in Linux](https://docs.microsoft.com/azure/virtual-machines/linux/expand-disks#expand-a-disk-partition-and-filesystem)<br>
* [LVM in Azure VMs](https://docs.microsoft.com/azure/virtual-machines/linux/configure-lvm)

### Managed Disks or conversion from unmanaged

* [Overview of Azure Managed Disks](https://docs.microsoft.com/azure/virtual-machines/linux/managed-disks-overview)<br>
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/linux/convert-unmanaged-to-managed-disks)<br>
* [FAQ for migrating to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/linux/faq-for-disks#migrate-to-managed-disks)

## **Recommended Documents**

* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)<br>
* [Understanding the temporary drive on your VM](https://docs.microsoft.com/azure/storage/storage-about-disks-and-vhds-linux#temporary-disk)<br>
* [Virtual Disks FAQ](https://docs.microsoft.com/azure/virtual-machines/linux/faq-for-disks)
