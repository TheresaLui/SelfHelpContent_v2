<properties
	pageTitle="Delete and Recover"
	description="Delete and Recover"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="malihaqu"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32551644,32551674,32551675"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public,MoonCake"
/>

# I need help deleting or recovering a storage object

## **Recommended steps**

### Deletion errors
You might receive an error when you try to delete the Azure storage account, container, or VHD in the Azure portal or the Azure classic portal. This issue may occur under the following circumstances:

- When you delete a VM, the disk and VHD are not automatically deleted. That might be the reason for failure on storage account deletion. We don’t delete the disk so that you can use the disk to mount another VM.<br>
- There is still a lease on a disk or the blob that's associated with the disk.<br>

If the storage account uses the ARM deployment model, you can remove the VHD by following these steps:

1. Go to Storage Account | Blobs | vhds, and locate the VHD that you want to delete, or that is preventing deletion of the container or storage account.  If you click on this VHD, it will show as Locked/Leased.
2. Determine which VM is currently using the leased VHD.  Generally, the name of the VHD will contain the name of the VM.
3. Go to Virtual Machine | Disks for the VM that has a lease on the VHD.  
4. Remove the VHD from the VM, which will allow the VHD to be deleted.  For OS Disks, you will need to delete the VM that is using the disk.  For Data Disks, click on the disk and select “Detach.”

### Recovery of deleted objects
- You may submit a support request to recover a deleted Storage Account | Blob Container within 14 days of deletion. We request that you do not attempt to recreate a storage account or blob container with the same name while we are attempting to recover.<br>
- Recovery of deleted or older versions of Files, Blobs, Tables and Queues is not currently supported.<br>


## **Recommended documents**
[I'm having problems deleting storage account](https://azure.microsoft.com/documentation/articles/storage-resource-manager-cannot-delete-storage-account-container-vhd/)
