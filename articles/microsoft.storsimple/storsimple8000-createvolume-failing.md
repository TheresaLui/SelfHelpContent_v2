<properties
	pageTitle="I can't create volumes or volume containers"
	description="I can't create volumes or volume containers"
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="8000Series"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="7e0a846f-7536-40c3-b59b-b2ed04ef394a"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# I can't create volumes or volume containers

If you cannot create volumes or volume containers, this could be due to one of the following reasons:

## **Recommended steps**

* Storage account is not set up properly. For detailed instructions, go to [Create a new storage account](https://docs.microsoft.com/azure/storage/storage-create-storage-account#create-a-storage-account).
* Storage account is deleted. Ensure that the storage account still exists and the associated credentials are correct.
* Storage account access keys have been regenerated. Ensure that you can access the storage account using the primary access key. If the keys have been regenerated, you will need to synchronize the new keys via the StorSimple Device Manager service. For detailed instructions, go to [Synchronize the keys for Storage accounts](https://docs.microsoft.com/azure/storsimple/storsimple-8000-manage-storage-accounts#key-rotation-of-storage-accounts).

## **Recommended documents**

[Tools for troubleshooting StorSimple deployments](https://docs.microsoft.com/azure/storsimple/storsimple-8000-troubleshoot-deployment#tools-for-troubleshooting-storsimple-deployments)<br>
[Use the Diagnostics tool to troubleshoot network connectivity](https://docs.microsoft.com/azure/storsimple/storsimple-8000-diagnostics)
