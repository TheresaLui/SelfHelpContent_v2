<properties
	pageTitle="How to check for backup or copy if customer has enabled Soft Delete for Blobs feature"
	description="How to check for backup or copy if customer has enabled Soft Delete for Blobs feature"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="34a9fc10-d168-42a2-9aec-424f052593fc"
/>

# How to check for backup or copy if customer has enabled Soft Delete for Blobs feature

1. Check if customer has enabled Soft Delete for Blobs feature "learn more"(https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-soft-delete)NOTE The soft delete feature state can also be checked in Azure Support Center. <br>
2. Navigate to the storage account in Resource Explorer. <br>
3. Look for value for Soft Delete Retention Enabled in the configuration section.<br>
4. If the feture is enabled and we have a specific blob that needs to be recovered, navigate to the storage account in Azure Support Center Resource Explorer and search for the specific blob from the Blobs tab. <br>
5. Soft deleted blobs listed will have the SOFT_DELETED flag.<br>
6. If found, customer can retrieve these blobs himself.<br>
7. Navigate to the container from the portal.<br>
8. Enable the "Show deleted blobs" checkbox to locate the deleted blobs.<br>
9. Right click on relevant blobs and choose Undelete.<br>

## Recommended Documents

1. [Azure_Storage_TSG_Recover Storage Account](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265682/Azure_Storage_TSG_Recover-Storage-Account)
2. [Data restore scenarios for Azure Storage service](https://support.microsoft.com/en-us/help/4012226/data-restore-scenarios-for-azure-storage-service)
