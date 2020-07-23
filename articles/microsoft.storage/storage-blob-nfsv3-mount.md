
<properties
	pageTitle="Network File System (NFS) 3.0 issues with Azure Blob storage"
    	description="Network File System (NFS) 3.0 issues with Azure Blob storage"
	service="microsoft.storage"
	resource="storage"
	authors="annayak"
	ms.author="annayak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32739611,32739612"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="a4914b88-2ad1-451c-94e0-137d852f0392"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Network File System (NFS) 3.0 mount issues with Azure Blob storage

4 out of 5 customers resolved their NFS mount issue using the steps listed below.

## **Recommended Documents**

- [How to sign up for the preview](https://docs.microsoft.com/azure/storage/blobs/network-file-system-protocol-support-how-to#step-1-register-the-nfs-30-protocol-feature-with-your-subscription)<br>

	>NFS 3.0 protocol support in Azure Blob storage is in public preview and is available in the following regions:<br>
	>[Currrent Regions](https://docs.microsoft.com/azure/storage/blobs/network-file-system-protocol-support)

- [Verify that the feature is registered](https://docs.microsoft.com/azure/storage/blobs/network-file-system-protocol-support-how-to#step-2-verify-that-the-feature-is-registered) using the following PowerShell cmdlets

	```powershell
	Get-AzProviderFeature -ProviderNamespace Microsoft.Storage -FeatureName AllowNFSV3
	Get-AzProviderFeature -ProviderNamespace Microsoft.Storage -FeatureName PremiumHns
	```

- [Types of Storage account supported for the preview](https://docs.microsoft.com/azure/storage/blobs/network-file-system-protocol-support-how-to#step-4-create-and-configure-a-storage-account)<br>
- [NFS 3.0 features not supported during the preview](https://docs.microsoft.com/azure/storage/blobs/network-file-system-protocol-support#nfs-30-features-not-yet-supported)<br>
- [Azure Storage features not supported during the preview](https://docs.microsoft.com/azure/storage/blobs/network-file-system-protocol-support#azure-storage-features-not-yet-supported)<br>
- [How to mount a storage container](https://docs.microsoft.com/azure/storage/blobs/network-file-system-protocol-support-how-to#step-6-mount-the-container)<br>
- [Pricing details](https://docs.microsoft.com/azure/storage/blobs/network-file-system-protocol-support#pricing)

### **Common Issues**

- [Resolve Common Issues](https://docs.microsoft.com/azure/storage/blobs/network-file-system-protocol-support-how-to#resolve-common-issues)

**Below are the most common reported issues currently**

| Issue/Error | Resolution |
|-|-|
| Access denied by server while mounting | Ensure that your client is running within a supported subnet. See the [Supported network locations](https://docs.microsoft.com/azure/storage/blobs/network-file-system-protocol-support#supported-network-connections) |
| No such file or directory | Ensure sure that the container that you're mounting was created after you verified that the feature was registered. See Step 2: [Verify that the feature is registered](https://docs.microsoft.com/azure/storage/blobs/network-file-system-protocol-support-how-to#step-2-verify-that-the-feature-is-registered).Also, make sure to type the mount command and it's parameters directly into the terminal. If you copy and paste any part of this command into the terminal from another application, hidden characters in the pasted information might cause this error to appear. |
| Files that were uploaded by using non-NFS 3.0 tools aren't visible in the directory. | Un-mount the container, and then mount the container again. |

