<properties
	pageTitle="Delete and Recover"
	description="Delete and Recover"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="malihaqu"
	displayOrder=""
	selfHelpType="resource"
	supportTopicIds=""
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

- Recovery of a deleted Storage Account may be attempted by submitting a support request immediately. There is no guarantee for recovery to be successful. We request that you do not attempt to recreate a Storage Account with the same name while we are attempting to recover.<br>
- For Storage Accounts configured with replication option: Geographically Redundant Storage (GRS) or Read-Access Geographically Redundant Storage (RA-GRS), recovery of a deleted Blob Container may be attempted by submitting a support request immediately. There is no guarantee for recovery to be successful. We request that you do not attempt to recreate a Blob Container with the same name while we are attempting to recover.<br>
- Recovery of deleted or older versions of Files, Blobs, Tables and Queues cannot be attempted.<br>

## **Recommended documents**
[I'm having problems deleting storage account](https://azure.microsoft.com/documentation/articles/storage-resource-manager-cannot-delete-storage-account-container-vhd/)<br>
[Delete Storage Account operation](https://msdn.microsoft.com/library/azure/hh264517.aspx)<br>
[Delete Container operation](https://docs.microsoft.com/rest/api/storageservices/delete-container)<br>

