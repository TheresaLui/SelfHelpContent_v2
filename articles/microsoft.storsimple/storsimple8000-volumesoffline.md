<properties
	pageTitle="My volumes have gone offline"
	description="My volumes have gone offline"
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="8000Series"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="3238bbf1-192c-4395-aba1-3ebdbb7a216c"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# My volumes have gone offline

If your volumes are offline, this could be due to one of the following reasons:

## **Recommended steps**

* Storage account is deleted. Ensure that the Storage account still exists and the associated credentials are correct.
* Storage account access keys have been regenerated. Ensure that you can access the storage account using the primary access key. If the keys have been regenerated, you will need to synchronize the new keys via the StorSimple Device Manager service. For detailed instructions, go to [Synchronize the keys for Storage accounts](https://docs.microsoft.com/azure/storsimple/storsimple-8000-manage-storage-accounts#key-rotation-of-storage-accounts).

## **Recommended documents**

[Use the StorSimple Device Manager service to manage your storage accounts](https://docs.microsoft.com/azure/storsimple/storsimple-8000-manage-storage-accounts)