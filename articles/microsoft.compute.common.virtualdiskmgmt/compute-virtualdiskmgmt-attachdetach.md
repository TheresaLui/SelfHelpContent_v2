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
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="d43073c5-75dc-4c03-b04a-aa4c56e765a8"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Resolving issues with VM Disk Management

4 out of 5 customers resolved their VM disk issue using the steps below.

## **Recommended Steps**

* **Attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-a-new-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#add-an-empty-data-disk-to-a-virtual-machine)
* [Initialize a new data disk in a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal#initialize-a-new-data-disk)
* **Attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-an-existing-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#attach-an-existing-data-disk-to-a-vm)
* **Detach a data disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-the-portall) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-powershell)
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/windows/find-unattached-disks)
* [Understanding the temporary disk on a VM](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview#temporary-disk)
* [Change the drive letter of the temporary disk](https://docs.microsoft.com/azure/virtual-machines/windows/change-drive-letter)

**NOTE**: When detaching a disk, remember to connect to the VM and **unmount the disk first**.

## **Recommended Documents**

* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)
* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#supported-vms)
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#premium-disks-managed-and-unmanaged)
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks)
