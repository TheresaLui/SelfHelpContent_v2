<properties
	pageTitle="Resolving issues with Virtual Disk Management Direct Upload"
	description="Resolving issues with Virtual Disk Management Direct Upload"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="timbasham"
	ms.author="tibasham"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32641057"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="compute-virtualdiskmgmt-directupload"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Resolving issues with Managed Disk direct upload

4 out of 5 customers resolved their VM virtual disk issue using the steps below.

## **Recommended Steps**

* [Upload a vhd to Azure using Azure PowerShell and AzCopy v10](https://docs.microsoft.com/azure/virtual-machines/windows/disks-upload-vhd-to-managed-disk-powershell)<br>
* [Upload a vhd to Azure using Azure CLI and AzCopy v10](https://docs.microsoft.com/azure/virtual-machines/linux/disks-upload-vhd-to-managed-disk-cli)<br>
* [Upload, download, cross-region copy managed disks using Azure Storage Explorer](https://docs.microsoft.com/azure/virtual-machines/windows/disks-use-storage-explorer-managed-disks)
* [Direct upload to a managed disk FAQ](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#uploading-to-a-managed-disk)<br>
* [Virtual Disks FAQ](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks)<br>

## **Recommended Documents**

### Attaching or detaching disks

* **Attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-a-new-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#add-an-empty-data-disk-to-a-virtual-machine)<br>
* [Initialize a new data disk in a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal#initialize-a-new-data-disk)<br>
* **Attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-an-existing-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#attach-an-existing-data-disk-to-a-vm)<br>
* **Detach a data disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-the-portall) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-powershell)<br>
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/windows/find-unattached-disks)<br>
* [Understanding the temporary disk on a VM](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview#temporary-disk)<br>
* [Change the drive letter of the temporary disk](https://docs.microsoft.com/azure/virtual-machines/windows/change-drive-letter)

**NOTE**: When detaching a disk, remember to connect to the VM and **unmount the disk first**.

### Premium Storage (SSD)

* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)<br>
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#supported-vms)<br>
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#premium-disks-managed-and-unmanaged)

### Increase or resize a disk attached to the VM (OS or data disk)

* [How to expand the OS disk of a VM](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk)<br>
* [Expand data disks for a VM](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk#resizing-data-disks)<br>
* [Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm)<br>
* [Convert between Standard and Premium storage for a disk](https://docs.microsoft.com/azure/virtual-machines/windows/convert-disk-storage)<br>
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#supported-vms)<br>
* [Extend a basic volume in Windows](https://docs.microsoft.com/windows-server/storage/disk-management/extend-a-basic-volume)<br>
* [Windows Storage Spaces](https://docs.microsoft.com/windows-server/storage/storage-spaces/overview)<br>
* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)

### Managed Disks or conversion from unmanaged

* [Overview of Azure Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview)<br>
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks)<br>
* [Plan for the conversion to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)<br>
* [Convert a VM from unmanaged disks to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)<br>
* [FAQ for migrating to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#migrate-to-managed-disks)