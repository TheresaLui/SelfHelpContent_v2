<properties
	pageTitle="Resolving issues with VM Disk Management"
	description="Resolving issues with VM Disk Management"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure,timbasham"
	ms.author="scotro,tibasham"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632143"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="139e0b4c-3609-4472-930e-e61306f5818e"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Resolving issues with VM Disk Management

4 out of 5 customers resolved their VM disk issue using the steps below.

## **Recommended Steps**

* Restore a VM from a managed snapshot using [PowerShell](https://docs.microsoft.com/azure/virtual-machines/scripts/virtual-machines-windows-powershell-sample-create-vm-from-snapshot)<br>
* Create a snapshot of a managed disk using the [Portal](https://docs.microsoft.com/azure/virtual-machines/windows/snapshot-copy-managed-disk#use-the-azure-portal), or [PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/snapshot-copy-managed-disk#use-powershell)<br>
* [Restore an unmanaged disk from snapshot](https://docs.microsoft.com/azure/virtual-machines/windows/incremental-snapshots#steps-to-restore-a-disk-from-snapshots)<br>
* [Create a snapshot of an unmanaged disk](https://docs.microsoft.com/azure/virtual-machines/windows/incremental-snapshots)<br>
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/windows/find-unattached-disks)

## **Recommended Documents**

* [Virtual Disks FAQ](https://docs.microsoft.com/azure/virtual-machines/windows/faq-for-disks)<br>
* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)<br>
* [Understanding the temporary drive on your VM](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview#temporary-disk)<br>
* [Overview of Azure Managed Disks](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview)<br>
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-managed-disks)
