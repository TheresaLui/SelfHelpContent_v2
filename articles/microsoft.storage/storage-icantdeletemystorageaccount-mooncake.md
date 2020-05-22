<properties
    pageTitle="I can't delete my storage account"
    description="I can't delete my storage account"
    service="microsoft.storage"
    resource="storageaccounts"
    authors="passaree"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="f3a1dd44-75eb-48c1-b0fc-b7f7bb153e7b"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# I can't delete my storage account

## **Recommended steps**

You might receive errors when you try to delete the Azure storage account, container, or VHD in the Azure portal or the Azure classic portal. The issues can be caused by the following circumstances:

* When you delete a VM, the disk and VHD are not automatically deleted. That might be the reason for failure on storage account deletion. We don’t delete the disk so that you can use the disk to mount another VM.
* There is still a lease on a disk or the blob that's associated with the disk.

If the storage account uses the ARM deployment model, you can remove the VHD by following these steps:

1. Go to Storage Account | Blobs | vhds, and locate the VHD that you want to delete, or that is preventing deletion of the container or storage account.  If you click on this VHD, it will show as Locked/Leased.
2. Determine which VM is currently using the leased VHD.  Generally, the name of the VHD will contain the name of the VM.
3. Go to Virtual Machine | Disks for the VM that has a lease on the VHD.  
4. Remove the VHD from the VM, which will allow the VHD to be deleted.  For OS Disks, you will need to delete the VM that is using the disk.  For Data Disks, click on the disk and select “Detach.”


## **Recommended documents**

* [I'm having problems deleting storage account](https://docs.azure.cn/storage/blobs/storage-troubleshoot-vhds)
