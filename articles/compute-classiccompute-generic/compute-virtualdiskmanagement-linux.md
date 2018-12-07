<properties
	pageTitle="Virtual Disk Management"
	description="Virtual Disk Management"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	authorAlias="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32411841,32602153,32602154"
	resourceTags="linux, redhat"
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="public"
/>

# Virtual Disk Management

4 out of 5 customers resolved their VM virtual disk issue using the below steps.<br>

**Need help with attaching or detaching disks**<br>

* Learn how to **attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-a-new-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-a-new-disk-to-a-vm)<br>
* Learn how to **attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-an-existing-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-an-existing-disk)<br>
* Learn how to **detach a data disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-the-portal) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-azure-cli).<br>
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/linux/find-unattached-disks)

	When detaching a VM, **remember** to connect to the VM and **unmount the disk first**.<br>

**Need help with Premium Storage (SSD)**<br>

* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#features)<br>
* [What VMs are supported for Premium Storage (SSD)](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#supported-vms)<br>
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/linux/faq-for-disks#premium-disks-managed-and-unmanaged)

**Issue with increasing the size or resize a disk attached to the VM (OS or data disk)**<br>

* [Expand virtual hard disks with Azure CLI](https://docs.microsoft.com/azure/virtual-machines/linux/expand-disks)<br>
* [Expand a disk partition and filesystem after expanding the virtual hard disk](https://docs.microsoft.com/azure/virtual-machines/linux/expand-disks#expand-a-disk-partition-and-filesystem)<br>

**Need help with Managed Disks or conversion from unmanaged**<br>

* [Overview of Azure Managed Disks](https://docs.microsoft.com/azure/virtual-machines/linux/managed-disks-overview)<br>
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks)<br>
* [Plan for the conversion to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)<br>
* [Convert a VM from unmanaged disks to managed disks](https://docs.microsoft.com/azure/virtual-machines/linux/convert-unmanaged-to-managed-disks)<br>
* [FAQ for migrating to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/linux/faq-for-disks#migrate-to-managed-disks)

## **Other Recommended Documents**

* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com//azure/virtual-machines/troubleshooting/allocation-failure)<br>
* [Learn how to resize a VM](https://docs.microsoft.com/azure/virtual-machines/linux/change-vm-size)<br>
* [Understanding the temporary drive on your VM](https://docs.microsoft.com/azure/storage/storage-about-disks-and-vhds-linux#temporary-disk)<br>
