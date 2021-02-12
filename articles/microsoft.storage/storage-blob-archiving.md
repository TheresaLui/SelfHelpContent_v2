<properties
	pageTitle="Archiving Azure Storage blob"
	description="Troubleshoot archiving Azure Storage blob"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
	ms.author="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602719"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="112a3653-ed44-40ea-bb56-5b137a937d03"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Upgrade to Azure Storage Account V2

## **Recommended steps**

- **Can I set my default account access tier to archive?**<br>
No. Only hot and cool storage tiers may be set as the default account access tier. Archive tier can only be set at the object level.

- **After setting the tier of a blob, when will I start getting billed at the appropriate rate?**<br>
Each blob is always billed according to the tier indicated by the blob's Access Tier property. When you set a new tier for a blob, the Access Tier property immediately reflects the new tier for all transitions. However, rehydrating a blob from the archive tier to a hot or cool tier can take several hours. In this case, you are billed at archive rates until rehydration is complete, at which point the Access Tier property reflects the new tier. At that point, you are billed for that blob at the hot or cool rate.


## **Recommended documents**
- [Azure Blob storage access tiers FAQ](https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers#faq)
- [Archive access tier](https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers#archive-access-tier)