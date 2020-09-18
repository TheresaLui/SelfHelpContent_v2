<properties
	pageTitle="Resolving issues with Linux Disk Management"
	description="Resolving issues with Linux Disk Management"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32730257"
	resourceTags=""
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="7f38987b-f7e0-4196-aaf6-b1d2e5f484e5"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Resolving issues with Linux Disk Management

4 out of 5 customers resolved their  disk issue using the steps below.

## **Recommended Steps**

Is your disk attached to the VM?
* **Attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-a-new-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-a-new-disk-to-a-vm)<br>
* **Attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-an-existing-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-an-existing-disk)

If this is a newly created VHD, have you initialized and formatted the disk yet?
* [Initialize a new data disk in a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#connect-to-the-linux-vm-to-mount-the-new-disk)

Need help with LVM?
* [Configure LVM on a Linux VM in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/configure-lvm)

Azure VM Temporary disk
* [Understanding the temporary disk on a VM](https://docs.microsoft.com/azure/storage/storage-about-disks-and-vhds-linux#temporary-disk)

Detach a data disk

    NOTE: When detaching a disk, remember to connect to the VM and unmount the disk first.
* [Detach using the Portal](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-the-portal)
* [Detach using CLI](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-azure-cli)

## **Recommended Documents**

* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/linux/convert-unmanaged-to-managed-disks)
* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#features)
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#supported-vms)
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/linux/faq-for-disks#premium-disks-managed-and-unmanaged)
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/linux/find-unattached-disks)
* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)
