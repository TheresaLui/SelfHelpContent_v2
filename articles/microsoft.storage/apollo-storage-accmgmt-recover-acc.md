<properties
    pageTitle="Recover deleted Storage Account"
    description="Recover deleted Storage Account Troubleshooting"
    infoBubbleText="See details on the right"
    service="microsoft.storage"
    resource="storage"
    authors="Lea"
    ms.author="leakkari"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32602701,32642178,32688873"
    resourceTags="recovery"
    productPesIds="15629,16459"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    articleId="f1f8e3a4-51ab-4165-a621-fbf2c6c2ceb1"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Recover deleted storage account

## Recovering your deleted storage account
Storage account recovery cases can now be resolved directly from the portal.

:::Section Recommended solutions::: 

### Recovery diagnostics 

<Insight> 
<symptomId>StorageRecoveryLightInsight</symptomId> 
<executionText>We are running a quick check to find out if your storage resource is recoverable</executionText> 
<timeoutText>We stopped the check, as it was taking too long</timeoutText> 
<noResultText>Our diagnostics did not find your storage resource. Please ensure the information provided is accurate and in the approved format. Also, check recommended solution below to find an answer.</noResultText> 
<additionalInputsReq>true</additionalInputsReq> 
</Insight> 


### Storage account recovery guideline 
You can initiate the recovery of your storage account directly from the portal. <br />
Follow [these instructions](https://docs.microsoft.com/azure/storage/common/storage-account-recover?toc=/azure/storage/blobs/toc.json) and click on the button below to recover your deleted storage account.
 
[Recover deleted storage account](button-data-blade:Microsoft_Azure_Storage.RecoverStorageAccountBlade.subscriptionId.$subscriptionId)​ <br />
 

**Note**: If you are trying to recover a storage account in a deleted resource group, **recreate the resource group first**. Recovery will fail if the resource group is not recreated.

### Container, Blob and Disk Recovery

1. Check if you have soft-delete enabled for your container/blob. If enabled, you can undelete your container/blob if you are still in your retention period. [Click here](https://docs.microsoft.com/azure/storage/blobs/soft-delete-blob-overview?WT.mc_id=Portal-Microsoft_Azure_Support) for instructions.
2. If soft-delete is not enabled, **your container/blob/disk can only be recovered if the following conditions are true**:

#### **Container** recovery:

1. The container was deleted in the last 14 days<br>
2. Storage account replication is configured as [GRS](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs), [RA-GRS](https://docs.microsoft.com/azure/storage/common/storage-redundancy-grs#read-access-geo-redundant-storage) or [GZRS](https://docs.microsoft.com/azure/storage/common/storage-redundancy-gzrs?toc=%2fazure%2fstorage%2fblobs%2ftoc.json) (We need the geo-replicated data for recovery):
3. A new storage object with the same name has not be re-created since deletion.

#### **Blob** and **disk** recovery:

1. This is a critical production data
2. Blob was deleted in the last:<br>
	* 7 days for standard storage<br>
	* 3 days for premium storage<br>
3. A new storage object with the same name has not be re-created since deletion. 

<br />
<br />

**Note**: It may not be possible to recover deleted data even if above conditions are true. As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten.Follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.

## **Recommended Documents**
* [Recovery of deleted storage account](https://docs.microsoft.com/azure/storage/common/storage-account-recover?toc=/azure/storage/blobs/toc.json)
* [Soft delete for Azure Storage blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete)
* [Recovery of deleted storage blob container](https://docs.microsoft.com/azure/storage/common/storage-account-container-recovery)

