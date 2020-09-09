<properties
	pageTitle="Storage configuration"
	description="Storage configuration"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,yareyes,amamun"	
	authors="ujpat,yareyes,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740103"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="30ad4466-56e3-422f-ab80-45c786b07719"
	ownershipId="AzureData_AzureSQLVM"
/>


# Storage configuration

4 out of 5 customers resolved their VM disk issue using the steps below.

## **Recommended Steps**

### Attaching or detaching disks

* **Attach a new disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-a-new-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#add-an-empty-data-disk-to-a-virtual-machine)
* [Initialize a new data disk in a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/attach-managed-disk-portal#initialize-a-new-data-disk)
* **Attach an existing disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-portal#attach-an-existing-disk) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/attach-disk-ps#attach-an-existing-data-disk-to-a-vm)
* **Detach a data disk** using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-the-portall) or [Powershell](https://docs.microsoft.com/azure/virtual-machines/windows/detach-disk#detach-a-data-disk-using-powershell)
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/windows/find-unattached-disks)
* [Understanding the temporary disk on a VM](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview#temporary-disk)
* [Change the drive letter of the temporary disk](https://docs.microsoft.com/azure/virtual-machines/windows/change-drive-letter)

**NOTE**: When detaching a disk, remember to connect to the VM and **unmount the disk first**.

### Premium Storage (SSD)

* [High-performance Premium Storage and managed disks for VMs](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#supported-vms)
* [FAQ for Premium disks: Managed and unmanaged](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#premium-disks-managed-and-unmanaged)

### Increase or resize a disk attached to the VM (OS or data disk)

* [How to expand the OS disk of a VM](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk)<br>
* [Expand data disks for a VM](https://docs.microsoft.com/azure/virtual-machines/windows/expand-os-disk#resizing-data-disks)<br>
* [Resize a Windows VM](https://docs.microsoft.com/azure/virtual-machines/windows/resize-vm)<br>
* [Convert between Standard and Premium storage for a disk](https://docs.microsoft.com/azure/virtual-machines/windows/convert-disk-storage)<br>
* [What VMs are supported for Premium Storage (SSD)?](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#supported-vms)<br>
* [Extend a basic volume in Windows](https://docs.microsoft.com/windows-server/storage/disk-management/extend-a-basic-volume)<br>
* [Windows Storage Spaces](https://docs.microsoft.com/windows-server/storage/storage-spaces/overview)

### Managed Disks or conversion from unmanaged

* [Overview of Azure Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview)
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks)
* [Plan for the conversion to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)
* [Convert a VM from unmanaged disks to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks#plan-for-the-conversion-to-managed-disks)
* [FAQ for migrating to Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks#migrate-to-managed-disks)

## **Recommended Documents**

* [Storage configuration for SQL Server VMs](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-server-storage-configuration)<br>
* [Azure Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/disks-types)
* [Virtual Disks FAQ](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks)<br>



