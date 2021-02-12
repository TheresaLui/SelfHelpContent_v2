<properties
	pageTitle="400 Block Blobs are not supported "
	description="400 Block Blobs are not supported "
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="e0503242-0e47-454b-bb49-1e1686863536"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# 400 Block Blobs are not supported 

1. You are moving data, block blobs, from standard v1 storage account to premium v2 storage account. During migration you see an error stating "400 Block blobs are not supported".
2.  The account type called "Premium" is actually "Premium Page Blobs". 
3. Verify the customer intends to move page blobs. GPv1 and GPv2 storage accounts only support page blobs (aka VHD). If not, educate customer about premium block blob storage if that's their intention. 
4. If using AzCopy v10. To specify blob type:
    1. Upload files as Append Blobs or Page Blobs.	--blob-type=[BlockBlob|PageBlob|AppendBlob]
    2. Upload to a specific access tier (such as the archive tier). 	--block-blob-tier=[None|Hot|Cool|Archive]

### Recommended Documents

1. [Performance tiers for block blob storage](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-performance-tiers)
2. [AzCopy v10 Copy blobs between storage accounts](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-blobs#copy-blobs-between-storage-accounts)
3. [Types of storage accounts](https://docs.microsoft.com/en-us/azure/storage/common/storage-account-overview#types-of-storage-accounts)
