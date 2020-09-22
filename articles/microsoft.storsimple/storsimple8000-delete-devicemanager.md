<properties
	pageTitle="I can't delete the StorSimple Device Manager or StorSimple device from Azure portal"
	description="I can't delete the StorSimple Device Manager or StorSimple device from Azure portal"
	service="microsoft.storsimple"
	resource="managers"
	authors="anbacker"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="8000Series"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ad191107-0163-4838-b754-201e1769d23b"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# I can't delete the StorSimple Device Manager or StorSimple device from Azure portal.


## **Recommended steps**

You can delete the StorSimple Device Manager service only if there are no devices connected to this service. Ensure that there are no registered devices and then retry the delete operation.

To delete a device, you need to first deactivate the device.

Before you deactivate the device, if you don't want to retain the cloud data associated with the device in the storage accounts, make sure that the device volumes, backup policies, and volume containers are deleted.

Once the device is deactivated, you can delete the device. This will allow you to avoid any usage charges for the device and the data.


## **Recommended documents**

[Delete a StorSimple Device Manager service](https://docs.microsoft.com/azure/storsimple/storsimple-8000-manage-service#delete-a-service)<br>
[Deactivate and delete a StorSimple device](https://docs.microsoft.com/azure/storsimple/storsimple-8000-deactivate-and-delete-device)