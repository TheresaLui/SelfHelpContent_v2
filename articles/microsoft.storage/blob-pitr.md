<properties
	pageTitle="How to conduct object replication"
	description="How to conduct object replication"
	service="microsoft.storage"
	resource="storage"
	authors="siz"
	ms.author="siz"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32742280"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="791666c1-1f53-4e56-8169-805704ec1db2"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# How to conduct point in time restore

## **Recommended Steps**

### **Preview Limitation**

- Restoring premium block blobs is not supported
- Restoring blobs in the archive tier is not supported. For example, if a blob in the hot tier was moved to the archive tier two days ago, and a restore operation restores to a point three days ago, the blob is not restored to the hot tier.
- Restoring Azure Data Lake Storage Gen2 flat and hierarchical namespaces is not supported
- Restoring storage accounts using customer-provided keys is not supported

## **Recommended Documents**

- [Pre-requisites for using point-in-time restore Feature](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-overview#prerequisites-for-point-in-time-restore)
- [Regions Availability & Preview Limitation](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-overview#about-the-preview)
- [How to enable point-in-time restore feature](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-manage)
- [How to perform a restore operation](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-manage#perform-a-restore-operation)
- [How to register for the preview](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-overview#register-for-the-preview)
- [Pricing and Billing information](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-overview#pricing-and-billing)
