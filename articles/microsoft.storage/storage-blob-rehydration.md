<properties
	pageTitle="Archiving Azure Storage blob"
	description="Troubleshoot archiving Azure Storage blob"
	infoBubbleText="See details on the right"
	service="microsoft.storage"
	resource="storage"
	authors="Passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602720"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public,MoonCake"
/>

# Upgrade to Azure Storage Account V2

## **Recommended steps**

**When rehydrating a blob from archive tier to the hot or cool tier, how will I know when rehydration is complete?**

During rehydration, you may use the get blob properties operation to poll the Archive Status attribute to confirm when the tier change is complete. The status reads "rehydrate-pending-to-hot" or "rehydrate-pending-to-cool" depending on the destination tier. Upon completion, the archive status property is removed, and the Access Tier blob property reflects the new hot or cool tier.

## **Recommended documents**
- [Azure Blob storage access tiers FAQ](https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers#faq)
- [Archive access tier](https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers#archive-access-tier)
- [Blob rehydration](https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers#blob-rehydration)