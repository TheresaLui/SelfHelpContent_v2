<properties
	pageTitle="I can't delete my storage account"
	description="I can't delete my storage account"
	service="microsoft.classicstorage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder="11"
	selfHelpType="resource"
	supportTopicIds="32551656"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="MoonCake"
/>

# I can't delete my storage account

## **Recommended steps**
You might receive errors when you try to delete the Azure storage account, container, or VHD in the Azure portal or the Azure classic portal. The issues can be caused by the following circumstances:

- When you delete a VM, the disk and VHD are not automatically deleted. That might be the reason for failure on storage account deletion. We don’t delete the disk so that you can use the disk to mount another VM.
- There is still a lease on a disk or the blob that's associated with the disk.

If the storage account uses the Classic deployment model, you can remove the virtual machine disk by following these steps:

1. Navigate to the [Azure portal](https://portal.azure.cn/)
2. Select VIRTUAL MACHINE > DISKS.
3. Locate the disks that are associated with the storage account, container, or VHD that you want to delete. When you check the location of the disk, you will find the associated storage account, container, or VHD.
4. Select your data disk, then click Delete Disk.
5. To delete disk images, navigate to the Images tab and delete any images that are stored in the account.

## **Recommended documents**
[I'm having problems deleting storage account](https://docs.azure.cn/storage/storage-resource-manager-cannot-delete-storage-account-container-vhd)
