<properties
    pageTitle="I can't delete my classic storage account"
    description="I can't delete my classic storage account"
    service="microsoft.classicstorage"
    resource="storageaccounts"
    authors="passaree"
    ms.author="passap"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds="32602689,32602694,32602738,32602712"
    resourceTags=""
    productPesIds="15629,16459"
    cloudEnvironments="MoonCake"
	articleId="35978720-59d8-4cf5-963b-4e64e08c4e19"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# I can't delete my classic storage account

## **Recommended Steps**

You might receive errors when you try to delete the Azure storage account, container, or VHD in the Azure portal or the Azure classic portal. The issues can be caused by the following circumstances:<br>

* When you delete a VM, the disk and VHD are not automatically deleted. This could cause the storage account deletion to fail. 
* There is still a lease on a disk or the blob that is associated with the disk

If the storage account uses the Classic deployment model, you can remove the virtual machine disk by following these steps:

1. Navigate to the [Azure portal](http://portal.azure.cn/)
2. Select VIRTUAL MACHINE > DISKS
3. Locate the disks that are associated with the storage account, container, or VHD that you want to delete. When you check the location of the disk, you will find the associated storage account, container, or VHD.
4. Select your data disk, then click Delete Disk
5. To delete disk images, navigate to the Images tab and delete any images that are stored in the account

## **Recommended Documents**

* [Troubleshooting disks attached to Azure VM](https://docs.azure.cn/zh-cn/storage/blobs/storage-troubleshoot-vhds)
