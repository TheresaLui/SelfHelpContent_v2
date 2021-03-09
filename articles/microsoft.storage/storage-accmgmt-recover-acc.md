<properties
    pageTitle="Recover deleted Storage Account"
    description="Recover deleted Storage Account Troubleshooting"
    infoBubbleText="See details on the right"
    service="microsoft.storage"
    resource="storage"
    authors="Lea Akkari"
    ms.author="leakkari"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32602701,32642178,32688873"
    resourceTags="recovery"
    productPesIds="15629,16459"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    articleId="e6c363fc-ee76-4afb-8278-bbb74b17051e"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Recover deleted storage data

## **Recommended Steps**

### **Storage Account Recovery**

You can initiate the recovery of your storage account directly from the Azure portal. <br />

   - Select the following button to recover your deleted storage account. Then, refer to [these instructions](https://docs.microsoft.com/azure/storage/common/storage-account-recover?toc=/azure/storage/blobs/toc.json).

   <a href="data-blade:Microsoft_Azure_Storage.RecoverStorageAccountBlade.subscriptionId.$subscriptionId"><button type="button" style="background-color:#1E90FF;color:white;width:240px; height:40px;"><b> Initiate Storage Account Recovery </b> </button></a>

   **Important:** To recover a storage account in a deleted resource group, re-create the resource group first or recovery will fail.

   <!-- ### [**Click here to recover a deleted storage account**](data-blade:Microsoft_Azure_Storage.RecoverStorageAccountBlade.subscriptionId.$subscriptionId) <br /> -->

### **Storage Data Recovery Guidelines**

Container, Blob and Disk Recovery

1. If soft-delete is enabled for your container/blob, and you are still in your retention period, you can undelete your container/blob. [Click here for instructions](https://docs.microsoft.com/azure/storage/blobs/soft-delete-blob-overview?WT.mc_id=Portal-Microsoft_Azure_Support).
2. If soft-delete is not enabled, your container/blob/disk can only be recovered if the following conditions are true:

   *Container recovery*

     - The container was deleted in the last 14 days<br>
     - Storage account replication is configured as [GRS](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs), [RA-GRS](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs#read-access-geo-redundant-storage) or [GZRS](https://docs.microsoft.com/azure/storage/common/storage-redundancy-gzrs?toc=%2fazure%2fstorage%2fblobs%2ftoc.json) (We need the geo-replicated data for recovery)
     - A new storage object with the same name has not been re-created since deletion.

   *Blob and disk recovery*

    1. This is a critical production data
    2. Blob was deleted in the last:<br>
	* 7 days for standard storage<br>
	* 3 days for premium storage<br>
    3. A new storage object with the same name has not be re-created since deletion. 

    Note: It may not be possible to recover deleted data even if above conditions are true. As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

### More resources

* [Recovery of deleted storage account](https://docs.microsoft.com/azure/storage/common/storage-account-recover?toc=/azure/storage/blobs/toc.json)
* [Soft delete for Azure Storage blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete)
