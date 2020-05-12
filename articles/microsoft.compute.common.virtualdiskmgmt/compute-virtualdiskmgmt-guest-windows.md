<properties
	pageTitle="Resolving issues with Windows Disk Management"
	description="Resolving issues with Windows Disk Management"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32730256"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="d5f62cb2-8caa-4b9a-b644-6f3fdf83e4c9"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Resolving issues with Windows Disk Management

4 out of 5 customers resolved their Windows disk issue using the steps below.

## **Recommended Steps**

Is your disk attached to the VM?
* **Attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-an-existing-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#attach-an-existing-data-disk-to-a-vm)
* **Attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-a-new-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#add-an-empty-data-disk-to-a-virtual-machine)

If this is a newly created VHD, have you initialized and formatted the disk yet?
* [Initialize a new data disk in a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal#initialize-a-new-data-disk)
* [Initialize a new disk](https://docs.microsoft.com/windows-server/storage/disk-management/initialize-new-disks)

Need help with a Storage Pool?
* [Storage Spaces FAQ](https://social.technet.microsoft.com/wiki/contents/articles/11382.storage-spaces-frequently-asked-questions-faq.aspx)
* [Storage Spaces](https://docs.microsoft.com/windows-server/storage/storage-spaces/overview)
* [Deploy Storage Spaces on a stand-alone server](https://docs.microsoft.com/windows-server/storage/storage-spaces/deploy-standalone-storage-spaces)

Common Windows disk management tasks
* [Change a drive letter](https://docs.microsoft.com/windows-server/storage/disk-management/change-a-drive-letter)
* [Extend a basic volume](https://docs.microsoft.com/windows-server/storage/disk-management/extend-a-basic-volume)

Troubleshooting Windows disk issues:
* [Troubleshooting issues with disks in Disk Management](https://docs.microsoft.com/windows-server/storage/disk-management/troubleshooting-disk-management)

Azure VM Temporary disk
* [Understanding the temporary disk on a VM](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview#temporary-disk)
* [Change the drive letter of the temporary disk](https://docs.microsoft.com/azure/virtual-machines/windows/change-drive-letter)

Detach a data disk

    NOTE: When detaching a disk, remember to connect to the VM and unmount the disk first.
* [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-the-portall)
* [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-powershell)



## **Recommended Documents**

* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks)
* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#supported-vms)
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#premium-disks-managed-and-unmanaged)
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/windows/find-unattached-disks)
* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)
