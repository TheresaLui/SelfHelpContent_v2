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

1. See [**How to register for the preview**](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-overview#register-for-the-preview)<br>

2. Register for the point-in time restore preview

	```powershell
	Register-AzProviderFeature -FeatureName RestoreBlobRanges -ProviderNamespace Microsoft.Storage
	```
	#### Register for change feed (preview)
	```powershell
	Register-AzProviderFeature -FeatureName Changefeed -ProviderNamespace Microsoft.Storage
	```
	#### Register for blob versioning (preview)
	```powershell
	Register-AzProviderFeature -ProviderNamespace Microsoft.Storage `
    -FeatureName Versioning
	```

	#### Refresh the Azure Storage provider namespace
	```powershell
	Register-AzResourceProvider -ProviderNamespace Microsoft.Storage
	```
	

- **How to check registration status**

	```powershell
	Get-AzProviderFeature -ProviderNamespace Microsoft.Storage `
    -FeatureName RestoreBlobRanges
	Get-AzProviderFeature -ProviderNamespace Microsoft.Storage `
    -FeatureName Changefeed
	Get-AzProviderFeature -ProviderNamespace Microsoft.Storage `
    -FeatureName Versioning

	```
- [**How to enable point-in time restore**](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-manage?tabs=portal)

 ### **Preview limitations and known issues**

 Learn more about [preview limitations and known issues](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-overview#limitations-and-known-issues).


## **Recommended Documents**

- [Prerequisites for using point-in-time restore Feature](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-overview#prerequisites-for-point-in-time-restore)
- [Regions Availability & Preview Limitation](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-overview#about-the-preview)
- [How to enable point-in-time restore feature](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-manage)
- [How to perform a restore operation](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-manage#perform-a-restore-operation)
- [How to register for the preview](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-overview#register-for-the-preview)
- [Pricing and Billing information](https://docs.microsoft.com/azure/storage/blobs/point-in-time-restore-overview#pricing-and-billing)
