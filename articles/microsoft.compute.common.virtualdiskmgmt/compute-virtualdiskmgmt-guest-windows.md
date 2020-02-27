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
	cloudEnvironments="public"
	articleId="d43073c5-75dc-4c03-b04a-aa4c56e765a8"
/>

# Resolving issues with Windows Disk Management

4 out of 5 customers resolved their Windows disk issue using the steps below.

## **Recommended Steps**

* [Initialize a new data disk in a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal#initialize-a-new-data-disk)
* [Initialize a new disk](https://docs.microsoft.com/windows-server/storage/disk-management/initialize-new-disks)
* [Change a drive letter](https://docs.microsoft.com/windows-server/storage/disk-management/change-a-drive-letter)
* [Extend a basic volume](https://docs.microsoft.com/windows-server/storage/disk-management/extend-a-basic-volume)
* [Troubleshooting issues with disks in Disk Management](https://docs.microsoft.com/windows-server/storage/disk-management/troubleshooting-disk-management)
* []()
* []()
* []()
* [Storage Spaces FAQ](https://social.technet.microsoft.com/wiki/contents/articles/11382.storage-spaces-frequently-asked-questions-faq.aspx)
* [Storage Spaces](https://docs.microsoft.com/windows-server/storage/storage-spaces/overview)
* [Deploy Storage Spaces on a stand-alone server](https://docs.microsoft.com/windows-server/storage/storage-spaces/deploy-standalone-storage-spaces)
* [Understanding the temporary disk on a VM](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview#temporary-disk)
* [Change the drive letter of the temporary disk](https://docs.microsoft.com/azure/virtual-machines/windows/change-drive-letter)

* **Attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-a-new-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#add-an-empty-data-disk-to-a-virtual-machine)
* **Attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-an-existing-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#attach-an-existing-data-disk-to-a-vm)
* **Detach a data disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-the-portall) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-powershell)
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/windows/find-unattached-disks)

**NOTE**: When detaching a disk, remember to connect to the VM and **unmount the disk first**.

## **Recommended Documents**

* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)
* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#supported-vms)
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#premium-disks-managed-and-unmanaged)
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks)
