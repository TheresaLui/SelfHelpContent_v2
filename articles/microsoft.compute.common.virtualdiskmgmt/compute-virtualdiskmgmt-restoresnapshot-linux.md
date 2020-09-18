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
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="3f754469-b316-40d3-9888-c36f5cdf51b5"
	ownershipId="Compute_VirtualMachines"
/>

# Resolving issues with VM Disk Management

4 out of 5 customers resolved their VM disk issue using the steps below.

## **Recommended Steps**

* Restore a VM from a managed snapshot using [CLI](https://docs.microsoft.com/azure/virtual-machines/scripts/virtual-machines-linux-cli-sample-create-vm-from-snapshot)<br>
* Create a snapshot of a managed disk using the [Portal](https://docs.microsoft.com/azure/virtual-machines/linux/snapshot-copy-managed-disk#use-azure-portal), or [CLI](https://docs.microsoft.com/azure/virtual-machines/linux/snapshot-copy-managed-disk#use-azure-cli)<br>
* [Restore an unmanaged disk from snapshot](https://docs.microsoft.com/azure/virtual-machines/linux/incremental-snapshots#steps-to-restore-a-disk-from-snapshots)<br>
* [Create a snapshot of an unmanaged disk](https://docs.microsoft.com/azure/virtual-machines/linux/incremental-snapshots)<br>
* [Find and delete unattached Azure managed and unmanaged disks](https://docs.microsoft.com/azure/virtual-machines/linux/find-unattached-disks)

## **Recommended Documents**

* [Virtual Disks FAQ](https://docs.microsoft.com/azure/virtual-machines/linux/faq-for-disks)<br>
* [Troubleshoot allocation failures when resizing a VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/allocation-failure)<br>
* [Understanding the temporary drive on your VM](https://docs.microsoft.com/azure/storage/storage-about-disks-and-vhds-linux#temporary-disk)<br>
* [Overview of Azure Managed Disks](https://docs.microsoft.com/azure/virtual-machines/linux/managed-disks-overview)<br>
* [Learn more about migrating to managed disks](https://docs.microsoft.com/azure/virtual-machines/linux/convert-unmanaged-to-managed-disks)
