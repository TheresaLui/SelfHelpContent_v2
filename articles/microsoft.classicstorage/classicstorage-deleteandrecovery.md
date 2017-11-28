<properties
	pageTitle="Delete and Recover"
	description="Delete and Recover"
	service="microsoft.classicstorage"
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
You might receive an error when you try to delete the Azure storage account, container, or VHD in the Azure portal or the Azure classic portal. This issue may occur under the following circumstances:

- When you delete a VM, the disk and VHD are not automatically deleted. That might be the reason for failure on storage account deletion. We don’t delete the disk so that you can use the disk to mount another VM.<br>
- There is still a lease on a disk or the blob that's associated with the disk.<br>

If the storage account uses the Classic deployment model, you can remove the virtual machine disk by following these steps:

1. Navigate to the [classic Azure portal](https://manage.windowsazure.com/)
2. Select VIRTUAL MACHINE > DISKS.
3. Locate the disks that are associated with the storage account, container, or VHD that you want to delete. When you check the location of the disk, you will find the associated storage account, container, or VHD.
4. Select your data disk, then click Delete Disk.
5. To delete disk images, navigate to the Images tab and delete any images that are stored in the account.

### Recovery of deleted objects
- You may submit a support request to recover a deleted Storage Account | Blob Container within 14 days of deletion. We request that you do not attempt to recreate a storage account or blob container with the same name while we are attempting to recover.<br>
- Recovery of deleted or older versions of Files, Blobs, Tables and Queues is not currently supported.<br>


## **Recommended documents**
[I'm having problems deleting classic storage account](http://go.microsoft.com/fwlink/?LinkId=785085)
