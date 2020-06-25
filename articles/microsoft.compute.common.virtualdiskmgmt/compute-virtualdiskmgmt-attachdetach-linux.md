<properties
	pageTitle="Resolving issues with VM Disk Management"
	description="Resolving issues with VM Disk Management"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure,timbasham"
	ms.author="scotro,tibasham"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632139,32632140"
	resourceTags=""
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="3cef1f67-f2f8-4a0e-887b-6a9aa09fcf27"
	ownershipId="Compute_VirtualMachines"
/>

# Resolving issues with VM Disk Management

4 out of 5 customers resolved their VM disk issue using the steps below.

## **Recommended Steps**

* **Attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-a-new-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-a-new-disk-to-a-vm)<br>
* [Initialize a new data disk in a Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#connect-to-the-linux-vm-to-mount-the-new-disk)<br>
* **Attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/attach-disk-portal#attach-an-existing-disk) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/add-disk#attach-an-existing-disk)<br>
* **Detach a data disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-the-portal) or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/detach-disk#detach-a-data-disk-using-azure-cli)<br>
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/linux/find-unattached-disks)<br>
* [Understanding the temporary disk on a VM](https://docs.microsoft.com/azure/storage/storage-about-disks-and-vhds-linux#temporary-disk)

**NOTE**: When detaching a disk, remember to connect to the VM and **unmount the disk first**.

## **Recommended Documents**

* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)<br>
* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#features)<br>
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/linux/premium-storage#supported-vms)<br>
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/linux/faq-for-disks#premium-disks-managed-and-unmanaged)<br>
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/linux/convert-unmanaged-to-managed-disks)
